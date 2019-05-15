# fdfs_client

使用：解压后放入python环境的LIB目录下
#test.py

from fdfs_client.client import Fdfs_client<br>
#client.conf是在etc/fdfs目录下copy过来的</br>
client = Fdfs_client('client.conf')<br/>
meta_dict={
    'ext_name'  : 'jpg'
}<br>
#file_ext_name指定文件后缀名<br>
res=client.upload_by_buffer(open('页面.png','rb').read(),file_ext_name='jpg')<br>
print(res)<br>
'''<br>
{'Group name': b'group1', 'Remote file_id': b'group1/M00/00/00/rBAAD1zFZ1yAGMPgAAVKFPwUKEA134.jpg',<br> 
'Status': 'Upload successed.', 'Local file name': '', 'Uploaded size': '338.52KB', 'Storage IP': b'129.204.237.5'}<br>
'''<br>

