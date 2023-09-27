# pybindtest

for making things running on Mac OS:
```ruby
pip install conan==1.59.0

mkdir build
cd build
conan install .. --output-folder cmake-build --build=missing -r conancenter
cmake .. -G "Xcode" -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake
cmake --build . --config Release
```

for testing, go to release folder:
```ruby
python
import example
example.pascal(8)
example.pascal(16)
example.pascal(22)
exit()
```
