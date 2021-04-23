---
title: Сообщение DRV_FREE (Ммсистем. h)
description: Уведомляет драйвер о том, что он удаляется из памяти. Драйвер должен освободить память и другие выделенные системные ресурсы.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989354"
---
# <a name="drv_free-message"></a><span data-ttu-id="e5e01-105">\_Свободное сообщение DRV</span><span class="sxs-lookup"><span data-stu-id="e5e01-105">DRV\_FREE message</span></span>

<span data-ttu-id="e5e01-106">Уведомляет драйвер о том, что он удаляется из памяти.</span><span class="sxs-lookup"><span data-stu-id="e5e01-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="e5e01-107">Драйвер должен освободить память и другие выделенные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e5e01-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5e01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e01-109"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="e5e01-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="e5e01-110">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="e5e01-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e01-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e01-111">Return Value</span></span>

<span data-ttu-id="e5e01-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e5e01-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e01-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5e01-113">Remarks</span></span>

<span data-ttu-id="e5e01-114">Параметры *двдриверид*, *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="e5e01-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="e5e01-115">Сообщение **DRV \_ Free** всегда является последним сообщением, которое получает драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="e5e01-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e01-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e5e01-116">Requirements</span></span>



| <span data-ttu-id="e5e01-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e5e01-117">Requirement</span></span> | <span data-ttu-id="e5e01-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e01-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e01-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5e01-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e01-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5e01-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5e01-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5e01-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e01-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5e01-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5e01-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5e01-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5e01-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5e01-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e01-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e01-126">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="e5e01-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="e5e01-127">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="e5e01-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





