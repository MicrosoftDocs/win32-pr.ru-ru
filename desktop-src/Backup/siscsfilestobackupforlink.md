---
title: Функция Сисксфилестобаккупфорлинк (Сисбкуп. h)
description: Возвращает сведения, описывающие файлы общего хранилища, на которые указывает ссылка SIS.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Резервное копирование функции Сисксфилестобаккупфорлинк
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654455"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="ff5b3-104">Функция Сисксфилестобаккупфорлинк</span><span class="sxs-lookup"><span data-stu-id="ff5b3-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="ff5b3-105">Функция **сисксфилестобаккупфорлинк** возвращает сведения, описывающие файлы общего хранилища, на которые указывает ссылка SIS.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5b3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff5b3-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="ff5b3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff5b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5b3-108">*сисбаккупструктуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-109">Указатель на структуру резервного копирования SIS, возвращенную из [**сискреатебаккупструктуре**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-110">*репарседата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-111">Указатель на содержимое точки повторного анализа SIS.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="ff5b3-112">Эта точка повторного анализа содержит данные, описывающие ссылку на SIS.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="ff5b3-113">Чтобы получить данные точки повторного анализа для файла, используйте управляющий код [**" \_ Получение \_ \_ точки**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) повторного анализа фсктл".</span><span class="sxs-lookup"><span data-stu-id="ff5b3-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-114">*репарседатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-115">Размер содержимого точки повторной обработки SIS, на которую указывает *репарседата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-116">*сисфилеконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-117">Указатель на строку контекста, предоставленную приложением резервного копирования, вызывающим эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="ff5b3-118">Содержимое этой строки содержимого полностью определяется этим приложением резервного копирования и не интерпретируется API резервного копирования SIS.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="ff5b3-119">Этот параметр является необязательным. Если не используется, присвойте этому параметру значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ff5b3-120">Значение этого параметра не будет обработано в этом случае.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-121">*матчингфилеконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-122">Удвоение — косвенный указатель на строку контекста ссылки SIS, идентифицируемую сведениями, передаваемыми в первых четырех параметрах этой функции.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="ff5b3-123">Этот параметр является необязательным. Если строка контекста не указана в качестве значения параметра *сисфилеконтекст* , установите для этого параметра значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ff5b3-124">Значение этого параметра не будет обработано в этом случае.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-125">*каунтофкоммонсторефилестобаккуп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-126">Число файлов, перечисленных в параметре *коммонсторефилестобаккуп* .</span><span class="sxs-lookup"><span data-stu-id="ff5b3-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-127">*коммонсторефилестобаккуп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-128">Указатель на массив имен файлов.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-128">Pointer to an array of file names.</span></span> <span data-ttu-id="ff5b3-129">Эти файлы следует архивировать одновременно и так же, как и файлы общего хранилища, запрашиваемые [**сискреатебаккупструктуре**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5b3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff5b3-130">Return value</span></span>

<span data-ttu-id="ff5b3-131">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="ff5b3-132">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff5b3-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff5b3-133">Remarks</span></span>

<span data-ttu-id="ff5b3-134">Приложение резервного копирования должно вызывать эту функцию только один раз для каждого файла ссылки SIS, для которого создается резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="ff5b3-135">Приложение резервного копирования может обнаруживать точку повторной обработки SIS по тегу, \_ ТЕГУ повторного анализа ввода-вывода \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ff5b3-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="ff5b3-136">Этот тег определен в Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="ff5b3-137">Если точка повторного анализа, определяемая значением параметра *репарседата* , описывает первый экземпляр файла для резервного копирования, эта функция возвращает **null** в качестве значения параметра *матчингфилеконтекст* и инициализирует значение массива строк *коммонсторефилестобаккуп* с именами файлов или файлов общего хранилища, для которых создается резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="ff5b3-138">В противном случае эта функция задаст значение параметра *матчингфилеконтекст* строке контекста, соответствующей первому экземпляру указанного файла, и присвойте параметру *каунтофкоммонсторефилестобаккуп* значение 0.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="ff5b3-139">Если существует несколько файлов общего хранилища, соответствующих указанной ссылке, значение параметра *сисфилеконтекст* будет строкой контекста, соответствующей первому файлу Common-Store, возвращенному в массиве, то есть коммонсторефилестобаккуп \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="ff5b3-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="ff5b3-140">Текущая версия этой функции будет возвращать не более одного файла общего хранилища, но в будущих версиях может существовать одна ссылка на несколько файлов общего хранилища, например по одному для каждого потока в файле, чтобы приложение резервного копирования поддерживало несколько файлов при каждом вызове этой функции.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="ff5b3-141">В любом случае каждый файл общего хранилища будет возвращаться не чаще одного раза для каждого этапа резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="ff5b3-142">Приложение резервного копирования должно выполнять резервное копирование или восстановление файлов или файлов общего хранилища, определенных по имени файла или именам файлов, возвращаемым в параметре *коммонсторефилестобаккуп* .</span><span class="sxs-lookup"><span data-stu-id="ff5b3-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="ff5b3-143">Независимо от того, существует ли соответствующий файл общего хранилища, приложение резервного копирования должно создать резервную копию файла канала SIS, так как он существует на диске, например, как точка повторного анализа и разреженный файл, и, скорее всего, не заполнены диапазонами.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="ff5b3-144">Приложение резервного копирования может немедленно выполнить резервное копирование или восстановление файлов или файлов общего хранилища, отложить их резервное копирование или при необходимости смешивать их вместе.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="ff5b3-145">После завершения операции резервного копирования следует освободить память, используемую массивом строк *коммонсторефилестобаккуп* , вызвав [**сисфриаллокатедмемори**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5b3-146">Требования</span><span class="sxs-lookup"><span data-stu-id="ff5b3-146">Requirements</span></span>



| <span data-ttu-id="ff5b3-147">Требование</span><span class="sxs-lookup"><span data-stu-id="ff5b3-147">Requirement</span></span> | <span data-ttu-id="ff5b3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ff5b3-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5b3-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff5b3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ff5b3-150">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ff5b3-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff5b3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ff5b3-152">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ff5b3-153">Header</span><span class="sxs-lookup"><span data-stu-id="ff5b3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff5b3-154"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b3-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff5b3-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff5b3-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff5b3-156"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b3-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff5b3-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ff5b3-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff5b3-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b3-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5b3-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff5b3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5b3-160">**сисфриаллокатедмемори**</span><span class="sxs-lookup"><span data-stu-id="ff5b3-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="ff5b3-161">**сискреатебаккупструктуре**</span><span class="sxs-lookup"><span data-stu-id="ff5b3-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

