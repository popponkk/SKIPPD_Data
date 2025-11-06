# SKIPPD_Data
用于存放处理过后的skippd数据

对于每个.npy文件都生成对应的.hdf5文件

因为 HDF5 不能原样存 object 数组，所以把时间戳的datetime格式换成固定长度19的字符串（S19）


skippd15mins:(粒度：1min，跨度：15min)
- trainval_images.npy: shape=(249555, 15, 64, 64, 3) | dtype=uint8 | load=mmap
- trainval_pvs.npy: shape=(249555, 30) | dtype=float64 | load=mmap
- trainval_times.npy: shape=(249555, 30) | dtype=object | load=pickle
  sample element type: datetime
- test_images.npy: shape=(13423, 15, 64, 64, 3) | dtype=uint8 | load=mmap
- test_pvs.npy: shape=(13423, 30) | dtype=float64 | load=mmap
- test_times.npy: shape=(13423, 30) | dtype=object | load=pickle
  sample element type: datetime

skippd4hs:(粒度：15min，跨度：4h)
- trainval_images_4h.npy: shape=(6563, 16, 64, 64, 3) | dtype=uint8 | load=mmap
- trainval_pvs_4h.npy: shape=(6563, 32) | dtype=float64 | load=mmap
- trainval_times_4h.npy: shape=(6563, 32) | dtype=object | load=pickle
  sample element type: datetime
- test_images_4h.npy: shape=(324, 16, 64, 64, 3) | dtype=uint8 | load=mmap
- test_pvs_4h.npy: shape=(324, 32) | dtype=float64 | load=mmap
- test_times_4h.npy: shape=(324, 32) | dtype=object | load=pickle
  sample element type: datetime