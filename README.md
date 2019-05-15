# fdfs_client
#example
from fdfs_client.client import Fdfs_client
#client.conf是在etc/fdfs目录下copy过来的

client = Fdfs_client('client.conf')
meta_dict={
    'ext_name'  : 'jpg'
}
#file_ext_name指定文件后缀名
res=client.upload_by_buffer(open('页面.png','rb').read(),file_ext_name='jpg')
print(res)
'''
{'Group name': b'group1', 'Remote file_id': b'group1/M00/00/00/rBAAD1zFZ1yAGMPgAAVKFPwUKEA134.jpg', 
'Status': 'Upload successed.', 'Local file name': '', 'Uploaded size': '338.52KB', 'Storage IP': b'129.204.....'}
'''
