# Kaggle-5-IFMO-study

- Статья автора:https://github.com/pfillard/tpx-kaggle-dsb2017

1. Скачать и устанивить cuda 8.0 и cudnn 5.1
  - https://medium.com/@ikekramer/installing-cuda-8-0-and-cudnn-5-1-on-ubuntu-16-04-6b9f284f6e77
  - Сuda по этой ставил: https://www.asozykin.ru/deep_learning/2017/02/26/how-to-install-cuda-8-on-ubuntu-16-04
  - cudNN по этой ставил https://github.com/RashmiTiwari132/CUDNN.git
  - Сuda качал от сюда: https://developer.nvidia.com/cuda-80-ga2-download-archive (Linux/x64_84/Ubuntu/16.04/runfile_local)
2. установка tensorflow r1.0_relu1 (здесь проблемы)
  - https://github.com/pfillard/tensorflow/tree/r1.0_relu1
  - https://www.tensorflow.org/install/install_sources
  - для того чтобы установить нужна програмка `bazel-0.4.5-installer-linux-x86_64.sh` качал через релиз на гите https://github.com/bazelbuild/bazel/releases/tag/0.4.5 (у меня получилось скачать только через свой пк, выложить на яндекс диск и скачать на сервер через `wget link -O bazel.zip` и потом `unzip bazel.zip`. Этот сайт поможет скачать на яндекс диск через ссылкy https://getfile.dokpub.com/yandex/)
  - кратко: качаем с гита, переходим на ветку, конфигурируем `./configure`, дальше надо скомпилировать `.whl` файл через `bazel build ...` и установить библиотеку через `pip3 `
  - при компиляции возникает ошибка: 
  ```
bazel build --config=opt //tensorflow/tools/pip_package:build_pip_package
INFO: Found 1 target...
[285 / 2,349] Still waiting for 200 jobs to complete:
Server terminated abruptly (error code: 14, error message: '', log file: '/root/.cache/bazel/_bazel_root/4d4b5309430ecf8c638c52fba28ae6e2/server/jvm.out')
  ```
3. все остальные пакеты через `pip3` ставятся нормально

4. Если разобраться, что за ошибка при компиляции tensorflow r1.0_relu1, то алгоритм должен запуститься.
