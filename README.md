## process

c++

java app 까지 만드는 예제 (tf꺼)

- https://github.com/tensorflow/examples/tree/master/lite/examples/digit_classifier





overall process

- https://utto.tistory.com/m/17?category=1080122
  - 대부분을 이걸 따름

- https://cppmagister.tistory.com/4
  - 이건 bazel configure 설정시 참고했음
  - 이사람 블로그에 android 앱으로 하는 방법 나와있음 참고

- https://stackoverflow.com/questions/56837288/tensorflow-lite-c-api-example-for-inference



bazel 이용

tf r2.1 버전 bazel 버전

- 소스에서 bazelversion 확인
  - 0.29.1



여기서 ndk 및 bazel configure 설정은 이거 참조하자

- https://cppmagister.tistory.com/6
  - 이때 난 android studio 이미 있었음



flat buffer 도 직접 설치해야하는 듯..

- https://stackoverflow.com/questions/55394537/how-to-install-flatc-and-flatbuffers-on-linux-ubuntu
- 그냥 flat buffer 아래처럼 빌드한 후에 통째로 복사했음

1. choice "folder for installation"
2. cd "folder for installation"
3. git clone https://github.com/google/flatbuffers.git
4. cd flatbuffers
5. cmake -G "Unix Makefiles" (install cmake if need)
6. make
7. sudo ln -s /full-path-to-flatbuffer/flatbuffers/flatc /usr/local/bin/flatc
8. chmod +x /full-path-to-flatbuffer/flatbuffers/flatc
9. run in any place as "flatc"



inference 시 input shape 등 설정은 tf 공식 코드 참조?

- https://github.com/tensorflow/tensorflow/issues/35357

- https://github.com/tensorflow/tensorflow/blob/master/tensorflow/lite/examples/label_image/label_image.cc
- https://github.com/tensorflow/tensorflow/blob/master/tensorflow/lite/examples/minimal/minimal.cc



의문

- tensorflow 나 flat buffer 꼭 내가 들고있어야함..?