Программа MyStem производит морфологический анализ текста на русском языке. 
MyStem умеет строить гипотетические разборы для множества слов — включая те слова, которых нет в словаре. 

**Форк narkq/php-mystem**, который успешно компилируется под Debian 9.9 (т.е. gcc 5+), а также под Debian 10 (gcc 10).

*Сборка и установка*:
```
wget https://github.com/yandex/tomita-parser/releases/download/v1.0/libmystem_c_binding.so.linux_x64.zip
unzip libmystem_c_binding.so.linux_x64.zip
sudo cp libmystem_c_binding.so /usr/local/lib64/
sudo ln -s /usr/local/lib64/libmystem_c_binding.so /usr/local/lib64/libmystem_c_binding.so.1
sudo apt-get -y install libicu-dev
cd php-mystem
phpize
./configure
make
sudo make install
```
Добавить в php.ini:
```
extension=mystem.so
```
