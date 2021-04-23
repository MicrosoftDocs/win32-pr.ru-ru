---
title: Метод использованием метода ibackgroundcopyjob Жетнопрогресстимеаут (Deliveryoptimization. h)
description: Возвращает время, в течение которого служба пытается переместить файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Метод Жетнопрогресстимеаут
- Метод Жетнопрогресстимеаут, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Жетнопрогресстимеаут
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490926"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="2fd46-107">Метод использованием метода ibackgroundcopyjob:: Жетнопрогресстимеаут</span><span class="sxs-lookup"><span data-stu-id="2fd46-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="2fd46-108">Возвращает время, в течение которого служба пытается переместить файл после возникновения временной ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fd46-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="2fd46-109">Если происходит выполнение, таймер сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="2fd46-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd46-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fd46-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2fd46-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fd46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd46-112">*претрипериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fd46-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd46-113">Время в секундах, в течение которого служба пытается переместить файл после возникновения временной ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fd46-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd46-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fd46-114">Return value</span></span>

<span data-ttu-id="2fd46-115">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="2fd46-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="2fd46-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2fd46-116">Return code</span></span>                                                                              | <span data-ttu-id="2fd46-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2fd46-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2fd46-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2fd46-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="2fd46-119">Время ожидания было успешно получено.</span><span class="sxs-lookup"><span data-stu-id="2fd46-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2fd46-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2fd46-120">Requirements</span></span>



| <span data-ttu-id="2fd46-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2fd46-121">Requirement</span></span> | <span data-ttu-id="2fd46-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2fd46-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd46-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fd46-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd46-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2fd46-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2fd46-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fd46-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd46-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2fd46-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2fd46-127">Header</span><span class="sxs-lookup"><span data-stu-id="2fd46-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd46-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd46-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fd46-129">IDL</span><span class="sxs-lookup"><span data-stu-id="2fd46-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fd46-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fd46-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2fd46-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2fd46-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fd46-132"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fd46-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2fd46-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd46-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd46-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd46-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2fd46-135">IID</span><span class="sxs-lookup"><span data-stu-id="2fd46-135">IID</span></span><br/>                      | <span data-ttu-id="2fd46-136">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="2fd46-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2fd46-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fd46-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd46-138">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="2fd46-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2fd46-139">**Использованием метода ibackgroundcopyjob:: Сетнопрогресстимеаут**</span><span class="sxs-lookup"><span data-stu-id="2fd46-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





