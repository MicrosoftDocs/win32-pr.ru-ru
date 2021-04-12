---
title: Метод IBackgroundCopyFile2 Жетфилеранжес (Deliveryoptimization. h)
description: Извлекает диапазоны, которые необходимо загрузить из удаленного файла.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Метод Жетфилеранжес
- Метод Жетфилеранжес, интерфейс IBackgroundCopyFile2
- Интерфейс IBackgroundCopyFile2, метод Жетфилеранжес
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415388"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="a788e-106">Метод IBackgroundCopyFile2:: Жетфилеранжес</span><span class="sxs-lookup"><span data-stu-id="a788e-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="a788e-107">Извлекает диапазоны, которые необходимо загрузить из удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="a788e-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a788e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a788e-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="a788e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a788e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a788e-110">*Ранжекаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a788e-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a788e-111">Число элементов в *диапазонах*.</span><span class="sxs-lookup"><span data-stu-id="a788e-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="a788e-112">*Диапазоны* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a788e-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a788e-113">Массив структур [**BG_FILE_RANGE**](bg-file-range.md) , указывающих диапазоны для загрузки.</span><span class="sxs-lookup"><span data-stu-id="a788e-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="a788e-114">По завершении вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения *диапазонов*.</span><span class="sxs-lookup"><span data-stu-id="a788e-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a788e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a788e-115">Return value</span></span>

<span data-ttu-id="a788e-116">Этот метод возвращает следующие возвращаемые значения, а также другие.</span><span class="sxs-lookup"><span data-stu-id="a788e-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="a788e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a788e-117">Return code</span></span>                                                                              | <span data-ttu-id="a788e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a788e-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a788e-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a788e-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="a788e-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="a788e-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="a788e-122">Не указаны диапазоны или задано задание отправки или отправки-ответа.</span><span class="sxs-lookup"><span data-stu-id="a788e-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="a788e-123">*Ранжекаунт* имеет нулевое значение, а для *Ranges* задано **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a788e-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a788e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a788e-124">Requirements</span></span>



| <span data-ttu-id="a788e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a788e-125">Requirement</span></span> | <span data-ttu-id="a788e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a788e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a788e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a788e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a788e-128">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a788e-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a788e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a788e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a788e-130">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a788e-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a788e-131">Header</span><span class="sxs-lookup"><span data-stu-id="a788e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a788e-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a788e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a788e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a788e-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a788e-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a788e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a788e-136"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a788e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a788e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a788e-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a788e-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a788e-139">IID</span><span class="sxs-lookup"><span data-stu-id="a788e-139">IID</span></span><br/>                      | <span data-ttu-id="a788e-140">IID_IBackgroundCopyFile2 определен как 83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="a788e-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a788e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a788e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a788e-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="a788e-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="a788e-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="a788e-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

