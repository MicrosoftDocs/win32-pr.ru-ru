---
title: Метод Ибаккграундкоперрор-File (Deliveryoptimization. h)
description: Извлекает указатель интерфейса на объект File, связанный с ошибкой.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Метод onfile
- Метод onfile, интерфейс Ибаккграундкоперрор
- Интерфейс Ибаккграундкоперрор, метод onfile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719192"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="d602e-106">Метод Ибаккграундкоперрор:: onfile</span><span class="sxs-lookup"><span data-stu-id="d602e-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="d602e-107">Извлекает указатель интерфейса на объект File, связанный с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d602e-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="d602e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d602e-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="d602e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d602e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d602e-110">*ппфиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d602e-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d602e-111">Указатель интерфейса [**ибаккграундкопифиле**](ibackgroundcopyfile.md) , методы которого используются для определения локальных и удаленных имен файлов, связанных с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d602e-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="d602e-112">Параметр *ппфиле* имеет значение **null** , если ошибка не связана с локальным или удаленным файлом.</span><span class="sxs-lookup"><span data-stu-id="d602e-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="d602e-113">По завершении выпустите *ппфиле*.</span><span class="sxs-lookup"><span data-stu-id="d602e-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d602e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d602e-114">Return value</span></span>

<span data-ttu-id="d602e-115">Этот метод возвращает следующие значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d602e-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="d602e-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d602e-116">Return code</span></span>                                                                                                | <span data-ttu-id="d602e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d602e-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d602e-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="d602e-119">Указатель интерфейса на объект файла успешно получен.</span><span class="sxs-lookup"><span data-stu-id="d602e-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d602e-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="d602e-121">Ошибка не связана с локальным или удаленным файлом.</span><span class="sxs-lookup"><span data-stu-id="d602e-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="d602e-122">Параметр *ппфиле* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d602e-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d602e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d602e-123">Requirements</span></span>



| <span data-ttu-id="d602e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d602e-124">Requirement</span></span> | <span data-ttu-id="d602e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d602e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d602e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d602e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d602e-127">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d602e-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d602e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d602e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d602e-129">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d602e-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d602e-130">Header</span><span class="sxs-lookup"><span data-stu-id="d602e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d602e-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d602e-132">IDL</span><span class="sxs-lookup"><span data-stu-id="d602e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d602e-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d602e-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d602e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d602e-135"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d602e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d602e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d602e-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d602e-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d602e-138">IID</span><span class="sxs-lookup"><span data-stu-id="d602e-138">IID</span></span><br/>                      | <span data-ttu-id="d602e-139">IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="d602e-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d602e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d602e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d602e-141">**ибаккграундкоперрор**</span><span class="sxs-lookup"><span data-stu-id="d602e-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="d602e-142">**Ибаккграундкоперрор:: возникла ошибка**</span><span class="sxs-lookup"><span data-stu-id="d602e-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





