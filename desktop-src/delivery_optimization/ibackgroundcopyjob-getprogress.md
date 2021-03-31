---
title: Метод использованием метода ibackgroundcopyjob метода Progress (Deliveryoptimization. h)
description: Извлекает сведения о ходе выполнения, связанные с заданием, такие как число переданных байтов и файлов.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Метод Progress
- Метод Progress, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Progress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136082"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="6e0df-106">Метод использованием метода ibackgroundcopyjob:: Progress</span><span class="sxs-lookup"><span data-stu-id="6e0df-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="6e0df-107">Извлекает сведения о ходе выполнения, связанные с заданием, такие как число переданных байтов и файлов.</span><span class="sxs-lookup"><span data-stu-id="6e0df-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0df-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e0df-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="6e0df-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e0df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0df-110">*ппрогресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6e0df-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0df-111">Содержит данные, которые можно использовать для вычисления процента завершенного задания.</span><span class="sxs-lookup"><span data-stu-id="6e0df-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0df-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e0df-112">Return value</span></span>

<span data-ttu-id="6e0df-113">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="6e0df-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="6e0df-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6e0df-114">Return code</span></span>                                                                              | <span data-ttu-id="6e0df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6e0df-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="6e0df-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6e0df-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6e0df-117">Сведения о ходе выполнения успешно получены.</span><span class="sxs-lookup"><span data-stu-id="6e0df-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e0df-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e0df-118">Requirements</span></span>



| <span data-ttu-id="6e0df-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e0df-119">Requirement</span></span> | <span data-ttu-id="6e0df-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e0df-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0df-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e0df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0df-122">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6e0df-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e0df-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e0df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0df-124">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6e0df-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6e0df-125">Header</span><span class="sxs-lookup"><span data-stu-id="6e0df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0df-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0df-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e0df-127">IDL</span><span class="sxs-lookup"><span data-stu-id="6e0df-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e0df-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e0df-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e0df-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6e0df-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e0df-130"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e0df-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6e0df-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6e0df-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e0df-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e0df-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6e0df-133">IID</span><span class="sxs-lookup"><span data-stu-id="6e0df-133">IID</span></span><br/>                      | <span data-ttu-id="6e0df-134">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="6e0df-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6e0df-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e0df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0df-136">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="6e0df-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





