---
title: Сообщение DRV_EXITSESSION (Ммсистем. h)
description: Уведомляет драйвер о том, что Windows готовится к выходу. Драйвер должен подготовиться к завершению.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- DRV_EXITSESSION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493041"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="1a32c-105">\_Екситсессион сообщение DRV</span><span class="sxs-lookup"><span data-stu-id="1a32c-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="1a32c-106">Уведомляет драйвер о том, что Windows готовится к выходу.</span><span class="sxs-lookup"><span data-stu-id="1a32c-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="1a32c-107">Драйвер должен подготовиться к завершению.</span><span class="sxs-lookup"><span data-stu-id="1a32c-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a32c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a32c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a32c-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="1a32c-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="1a32c-110">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="1a32c-110">Identifier of the installable driver.</span></span> <span data-ttu-id="1a32c-111">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="1a32c-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="1a32c-112"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="1a32c-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="1a32c-113">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="1a32c-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a32c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a32c-114">Return Value</span></span>

<span data-ttu-id="1a32c-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1a32c-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a32c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a32c-116">Remarks</span></span>

<span data-ttu-id="1a32c-117">Параметры *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="1a32c-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a32c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1a32c-118">Requirements</span></span>



| <span data-ttu-id="1a32c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1a32c-119">Requirement</span></span> | <span data-ttu-id="1a32c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a32c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a32c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a32c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a32c-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a32c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a32c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a32c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a32c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a32c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1a32c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1a32c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a32c-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a32c-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a32c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a32c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a32c-128">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="1a32c-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="1a32c-129">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="1a32c-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





