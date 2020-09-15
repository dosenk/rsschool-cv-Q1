# Dmitry Osipenko
### Contact:
  - Email: dmtr.osipenko@gmail.com
  - Telegram: @dosenk
  
### SKILLS:
  - PHP 
  - Linux (Ubuntu/Debian, Centos/RedHat)
  - Mysql
  - Apache
  - Nginx
  - Docker
  - KVM (Proxmox)
```PHP
class data
{
    public $path;
    public $fileType;
    public $fileName;
    private $_fileError;
    private $_fileTmpName;

    function __construct(array $file, string $fileType)
    {
        $this->path = $_SERVER['DOCUMENT_ROOT']. '/logger/files/'.$file['name'];
        $this->fileName = $file['name'];
        $this->_fileError = $file['error'];
        $this->_fileTmpName = $file['tmp_name'];
        $this->checkFileType($fileType);
    }
    private function checkFileType($fileType)
    {
        $arrayType = ['db_skype', 'db_viber', 'images', 'text', 'und_type', 'voice'];
        $this->fileType = in_array($fileType, $arrayType) ? $fileType : 'und_type';
    }

    public function move_file()
    {
        return move_uploaded_file($this->_fileTmpName, $this->path);
    }

}
```
### Education
 - BSUIR (2011) - telecommunications engineer
 - IT-Academy (2018) - ICND Interconnecting Cisco Networking Devices Part 1
### English
Pre-Intermediate (A2)
