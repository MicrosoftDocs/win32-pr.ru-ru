---
title: Сообщение DRV_POWER (Ммсистем. h)
description: Уведомляет драйвер о том, что питание устройства включено или выключено.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- DRV_POWER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989350"
---
# <a name="drv_power-message"></a><span data-ttu-id="136e5-104">DRV, \_ сообщение о питании</span><span class="sxs-lookup"><span data-stu-id="136e5-104">DRV\_POWER message</span></span>

<span data-ttu-id="136e5-105">Уведомляет драйвер о том, что питание устройства включено или выключено.</span><span class="sxs-lookup"><span data-stu-id="136e5-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="136e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="136e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="136e5-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="136e5-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="136e5-108">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="136e5-108">Identifier of the installable driver.</span></span> <span data-ttu-id="136e5-109">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="136e5-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="136e5-110"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="136e5-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="136e5-111">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="136e5-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="136e5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="136e5-112">Return Value</span></span>

<span data-ttu-id="136e5-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="136e5-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="136e5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="136e5-114">Remarks</span></span>

<span data-ttu-id="136e5-115">Параметры *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="136e5-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="136e5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="136e5-116">Requirements</span></span>



| <span data-ttu-id="136e5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="136e5-117">Requirement</span></span> | <span data-ttu-id="136e5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="136e5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136e5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="136e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="136e5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="136e5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="136e5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="136e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="136e5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="136e5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="136e5-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="136e5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="136e5-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="136e5-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136e5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="136e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136e5-126">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="136e5-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="136e5-127">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="136e5-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





