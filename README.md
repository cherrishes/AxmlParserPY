# AxmlParserPY
axmlparserpy,Android的XML解析器的Python实现
# -------------------------------------------------------------------
# version: 0.0.1
# -------------------------------------------------------------------

Example: 

1. convert apk binary manifest to string manifest.

import axmlparserpy.axmlprinter as axmlprinter

  ap = axmlprinter.AXMLPrinter(open('example/binary/AndroidManifest.xml', 'rb').read())
  buff = minidom.parseString(ap.getBuff()).toxml()
  print(buff)

2. get apk information
import axmlparserpy.apk as apk
  ap = apk.APK('_PATH_TO_APK')
  print （ap.get_package()）
  print （ap.get_androidversion_name()）
