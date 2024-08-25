https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite/issues/112
解决这个问题
![image](https://github.com/user-attachments/assets/4f160e16-d1b0-4c82-adbf-cc3ad33bd330)
![image](https://github.com/user-attachments/assets/8c1d60c2-0e3b-4063-8839-bbc5daa21883)
![image](https://github.com/user-attachments/assets/fbf6ca07-190a-470f-81be-f976045bf54e)

解决方法在
ComfyUI\custom_nodes\ComfyUI-VideoHelperSuite\videohelpersuite目录下
修改目录下的nodes.py
/ComfyUI/custom_nodes/ComfyUI-VideoHelperSuite/videohelpersuite/nodes.py
将kwargs由
kwargs = prompt[unique_id]['inputs']
改为
kwargs = {'frame_rate': 25, 'loop_count': 0, 'filename_prefix': 'pexelsdance1-', 'format': 'video/h264-mp4', 'pix_fmt': 'yuv420p', 'crf': 19, 'save_metadata': True, 'pingpong': False, 'save_output': True, 'images': ['10', 0]}
然后运行comfyui目录下带视频助手节点的代码
生成的代码可正常运行
![image](https://github.com/user-attachments/assets/ddb2747b-6c7d-4364-aa53-ea117a1cc934)

