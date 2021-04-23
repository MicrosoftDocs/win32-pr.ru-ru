---
title: Сообщение DRV_REMOVE (Ммсистем. h)
description: Уведомляет драйвер о том, что он собирается удалить из системы. Когда драйвер получает это сообщение, он должен удалить все разделы, созданные в реестре.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072005"
---
# <a name="drv_remove-message"></a><span data-ttu-id="55ab9-105">DRV \_ Удалить сообщение</span><span class="sxs-lookup"><span data-stu-id="55ab9-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="55ab9-106">Уведомляет драйвер о том, что он собирается удалить из системы.</span><span class="sxs-lookup"><span data-stu-id="55ab9-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="55ab9-107">Когда драйвер получает это сообщение, он должен удалить все разделы, созданные в реестре.</span><span class="sxs-lookup"><span data-stu-id="55ab9-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="55ab9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="55ab9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ab9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="55ab9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="55ab9-110">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="55ab9-110">Identifier of the installable driver.</span></span> <span data-ttu-id="55ab9-111">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="55ab9-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="55ab9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="55ab9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="55ab9-113">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="55ab9-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ab9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55ab9-114">Return Value</span></span>

<span data-ttu-id="55ab9-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="55ab9-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ab9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55ab9-116">Remarks</span></span>

<span data-ttu-id="55ab9-117">Параметры *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="55ab9-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ab9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="55ab9-118">Requirements</span></span>



| <span data-ttu-id="55ab9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="55ab9-119">Requirement</span></span> | <span data-ttu-id="55ab9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="55ab9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ab9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55ab9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="55ab9-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55ab9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="55ab9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55ab9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="55ab9-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55ab9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="55ab9-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55ab9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="55ab9-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55ab9-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ab9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55ab9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ab9-128">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="55ab9-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="55ab9-129">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="55ab9-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





