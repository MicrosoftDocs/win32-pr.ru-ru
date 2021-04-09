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
# <a name="adding-files-to-a-job"></a><span data-ttu-id="3acda-105">Добавление файлов в задание</span><span class="sxs-lookup"><span data-stu-id="3acda-105">Adding Files to a Job</span></span>

<span data-ttu-id="3acda-106">Задание содержит один или несколько файлов, которые требуется переместить.</span><span class="sxs-lookup"><span data-stu-id="3acda-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="3acda-107">Для добавления файлов в задание используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="3acda-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="3acda-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="3acda-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="3acda-109">Добавляет один файл в задание.</span><span class="sxs-lookup"><span data-stu-id="3acda-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="3acda-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Использованием метода ibackgroundcopyjob:: Аддфилесет**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="3acda-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="3acda-111">Добавляет один или несколько файлов в задание.</span><span class="sxs-lookup"><span data-stu-id="3acda-111">Adds one or more files to a job.</span></span> <span data-ttu-id="3acda-112">При добавлении нескольких файлов более эффективно вызывать этот метод, чем вызывать метод **AddFile** в цикле.</span><span class="sxs-lookup"><span data-stu-id="3acda-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="3acda-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3:: Аддфилевисранжес**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="3acda-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="3acda-114">Добавляет один файл в задание.</span><span class="sxs-lookup"><span data-stu-id="3acda-114">Adds a single file to a job.</span></span> <span data-ttu-id="3acda-115">Используйте этот метод, если требуется загрузить диапазоны данных из файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="3acda-116">Этот метод можно использовать только для загрузки заданий.</span><span class="sxs-lookup"><span data-stu-id="3acda-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="3acda-117">При добавлении файла в задание указывается удаленное имя и локальное имя файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="3acda-118">Дополнительные сведения о формате локальных и удаленных имен файлов см. в разделе Структура [**\_ \_ сведений о файле BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .</span><span class="sxs-lookup"><span data-stu-id="3acda-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="3acda-119">Задание отправки может содержать только один файл.</span><span class="sxs-lookup"><span data-stu-id="3acda-119">An upload job can contain only one file.</span></span> <span data-ttu-id="3acda-120">Методы [**использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) и [**использованием метода ibackgroundcopyjob:: АДДФИЛЕСЕТ**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) возвращают BG \_ E \_ слишком \_ много \_ файлов, если вы попытаетесь добавить в задание передачи более одного файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="3acda-121">Если необходимо передать более одного файла, рассмотрите возможность использования CAB-файла или ZIP.</span><span class="sxs-lookup"><span data-stu-id="3acda-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="3acda-122">Для заданий скачивания BITS ограничивает количество файлов, которые пользователь может добавить в задание, в 200 файлов и число диапазонов для файла в диапазоне 500.</span><span class="sxs-lookup"><span data-stu-id="3acda-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="3acda-123">Эти ограничения не применяются к администраторам и службам.</span><span class="sxs-lookup"><span data-stu-id="3acda-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="3acda-124">Сведения об изменении этих ограничений по умолчанию см. в разделе [групповые политики](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3acda-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="3acda-125">Владелец задания или пользователь с правами администратора может добавлять файлы в задание в любое время до вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) или метода [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="3acda-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="3acda-126">Если необходимо изменить удаленное имя файла после добавления файла в задание, можно вызвать метод [**IBackgroundCopyJob3:: реплацеремотепрефикс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) или метод [**IBackgroundCopyFile2:: сетремотенаме**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) .</span><span class="sxs-lookup"><span data-stu-id="3acda-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="3acda-127">Используйте метод **реплацеремотепрефикс** , чтобы изменить серверную часть удаленного имени, если сервер недоступен, или разрешить пользователям роуминга подключаться к ближайшему серверу.</span><span class="sxs-lookup"><span data-stu-id="3acda-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="3acda-128">Используйте метод **сетремотенаме** для изменения протокола, используемого для перемещения файла, или для изменения имени или пути файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="3acda-129">Служба BITS создает временный файл в целевом каталоге и использует временный файл для передачи файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="3acda-130">Чтобы получить имя временного файла, вызовите метод [**IBackgroundCopyFile3:: жеттемпораринаме**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) .</span><span class="sxs-lookup"><span data-stu-id="3acda-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="3acda-131">При вызове метода [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) служба BITS изменяет имя временного файла на имя целевого файла.</span><span class="sxs-lookup"><span data-stu-id="3acda-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="3acda-132">При [**создании**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) временного файла служба BITS не задает дескриптор безопасности (файл наследует данные ACL из каталога назначения).</span><span class="sxs-lookup"><span data-stu-id="3acda-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="3acda-133">Если передаваемые данные конфиденциальны, приложение должно указать соответствующий список ACL в целевом каталоге, чтобы предотвратить несанкционированный доступ.</span><span class="sxs-lookup"><span data-stu-id="3acda-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="3acda-134">Чтобы сохранить сведения о владельце и списке управления доступом для переданного файла, вызовите метод [**IBackgroundCopyJob3:: сетфилеаклфлагс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .</span><span class="sxs-lookup"><span data-stu-id="3acda-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="3acda-135">Владелец задания (пользователь, создавший задание или администратор, выполнивший [владение](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) этим заданием) должен иметь разрешения на доступ к файлу на сервере, а также к клиенту.</span><span class="sxs-lookup"><span data-stu-id="3acda-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="3acda-136">Например, чтобы скачать файл, пользователь должен иметь разрешения на чтение на сервере и разрешения на запись в локальный каталог на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3acda-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="3acda-137">В следующем примере показано, как добавить один файл в задание.</span><span class="sxs-lookup"><span data-stu-id="3acda-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="3acda-138">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) пжоб является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3acda-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


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



<span data-ttu-id="3acda-139">В следующем примере показано, как добавить в задание несколько файлов.</span><span class="sxs-lookup"><span data-stu-id="3acda-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="3acda-140">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , пжоб, является допустимым и локальные и удаленные имена берутся из списка в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3acda-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


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



 

 