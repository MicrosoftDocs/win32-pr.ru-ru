---
title: Метод использованием метода ibackgroundcopyjob Енумфилес (Deliveryoptimization. h)
description: Извлекает указатель интерфейса Иенумбаккграундкопифилес, используемый для перечисления файлов в задании.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Метод Енумфилес
- Метод Енумфилес, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Енумфилес
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136162"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="c4cb4-106">Метод использованием метода ibackgroundcopyjob:: Енумфилес</span><span class="sxs-lookup"><span data-stu-id="c4cb4-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="c4cb4-107">Извлекает указатель интерфейса [**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md) , используемый для перечисления файлов в задании.</span><span class="sxs-lookup"><span data-stu-id="c4cb4-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cb4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4cb4-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="c4cb4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4cb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4cb4-110">*ппенумфилес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4cb4-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4cb4-111">Указатель интерфейса [**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md) , который используется для перечисления файлов в задании.</span><span class="sxs-lookup"><span data-stu-id="c4cb4-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="c4cb4-112">Выпустите *ппенумфилес* по завершении.</span><span class="sxs-lookup"><span data-stu-id="c4cb4-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4cb4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4cb4-113">Return value</span></span>

<span data-ttu-id="c4cb4-114">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="c4cb4-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cb4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c4cb4-115">Requirements</span></span>



| <span data-ttu-id="c4cb4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c4cb4-116">Requirement</span></span> | <span data-ttu-id="c4cb4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cb4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cb4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4cb4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cb4-119">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4cb4-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4cb4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4cb4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cb4-121">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4cb4-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c4cb4-122">Header</span><span class="sxs-lookup"><span data-stu-id="c4cb4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4cb4-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4cb4-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4cb4-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c4cb4-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4cb4-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4cb4-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4cb4-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4cb4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4cb4-127"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4cb4-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c4cb4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c4cb4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4cb4-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4cb4-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c4cb4-130">IID</span><span class="sxs-lookup"><span data-stu-id="c4cb4-130">IID</span></span><br/>                      | <span data-ttu-id="c4cb4-131">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c4cb4-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c4cb4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4cb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cb4-133">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="c4cb4-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c4cb4-134">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="c4cb4-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





