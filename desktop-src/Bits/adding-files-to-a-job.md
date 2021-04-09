---
title: Добавление файлов в задание
description: Задание содержит один или несколько файлов, которые требуется переместить.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- передачи битов заданий, Добавление файлов
- БИТЫ передачи файлов, добавление
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987653"
---
# <a name="adding-files-to-a-job"></a>Добавление файлов в задание

Задание содержит один или несколько файлов, которые требуется переместить. Для добавления файлов в задание используйте один из следующих методов.

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Добавляет один файл в задание.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Использованием метода ibackgroundcopyjob:: Аддфилесет**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Добавляет один или несколько файлов в задание. При добавлении нескольких файлов более эффективно вызывать этот метод, чем вызывать метод **AddFile** в цикле.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3:: Аддфилевисранжес**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Добавляет один файл в задание. Используйте этот метод, если требуется загрузить диапазоны данных из файла. Этот метод можно использовать только для загрузки заданий.

</dd> </dl>

При добавлении файла в задание указывается удаленное имя и локальное имя файла. Дополнительные сведения о формате локальных и удаленных имен файлов см. в разделе Структура [**\_ \_ сведений о файле BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .

Задание отправки может содержать только один файл. Методы [**использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) и [**использованием метода ibackgroundcopyjob:: АДДФИЛЕСЕТ**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) возвращают BG \_ E \_ слишком \_ много \_ файлов, если вы попытаетесь добавить в задание передачи более одного файла. Если необходимо передать более одного файла, рассмотрите возможность использования CAB-файла или ZIP.

Для заданий скачивания BITS ограничивает количество файлов, которые пользователь может добавить в задание, в 200 файлов и число диапазонов для файла в диапазоне 500. Эти ограничения не применяются к администраторам и службам. Сведения об изменении этих ограничений по умолчанию см. в разделе [групповые политики](group-policies.md).

Владелец задания или пользователь с правами администратора может добавлять файлы в задание в любое время до вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) или метода [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .

Если необходимо изменить удаленное имя файла после добавления файла в задание, можно вызвать метод [**IBackgroundCopyJob3:: реплацеремотепрефикс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) или метод [**IBackgroundCopyFile2:: сетремотенаме**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) . Используйте метод **реплацеремотепрефикс** , чтобы изменить серверную часть удаленного имени, если сервер недоступен, или разрешить пользователям роуминга подключаться к ближайшему серверу. Используйте метод **сетремотенаме** для изменения протокола, используемого для перемещения файла, или для изменения имени или пути файла.

Служба BITS создает временный файл в целевом каталоге и использует временный файл для передачи файла. Чтобы получить имя временного файла, вызовите метод [**IBackgroundCopyFile3:: жеттемпораринаме**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) . При вызове метода [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) служба BITS изменяет имя временного файла на имя целевого файла. При [**создании**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) временного файла служба BITS не задает дескриптор безопасности (файл наследует данные ACL из каталога назначения). Если передаваемые данные конфиденциальны, приложение должно указать соответствующий список ACL в целевом каталоге, чтобы предотвратить несанкционированный доступ.

Чтобы сохранить сведения о владельце и списке управления доступом для переданного файла, вызовите метод [**IBackgroundCopyJob3:: сетфилеаклфлагс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .

Владелец задания (пользователь, создавший задание или администратор, выполнивший [владение](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) этим заданием) должен иметь разрешения на доступ к файлу на сервере, а также к клиенту. Например, чтобы скачать файл, пользователь должен иметь разрешения на чтение на сервере и разрешения на запись в локальный каталог на клиенте.

В следующем примере показано, как добавить один файл в задание. В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) пжоб является допустимым.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



В следующем примере показано, как добавить в задание несколько файлов. В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , пжоб, является допустимым и локальные и удаленные имена берутся из списка в пользовательском интерфейсе.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 