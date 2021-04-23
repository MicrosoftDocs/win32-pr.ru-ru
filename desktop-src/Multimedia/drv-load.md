---
title: Сообщение DRV_LOAD (Ммсистем. h)
description: Уведомляет драйвер о том, что он был загружен. Драйвер должен убедиться в наличии оборудования и вспомогательных драйверов, необходимых для правильной работы.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989352"
---
# <a name="drv_load-message"></a><span data-ttu-id="70418-105">\_Сообщение о загрузке DRV</span><span class="sxs-lookup"><span data-stu-id="70418-105">DRV\_LOAD message</span></span>

<span data-ttu-id="70418-106">Уведомляет драйвер о том, что он был загружен.</span><span class="sxs-lookup"><span data-stu-id="70418-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="70418-107">Драйвер должен убедиться в наличии оборудования и вспомогательных драйверов, необходимых для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="70418-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="70418-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70418-108">Parameters</span></span>

<span data-ttu-id="70418-109">Параметр *хдрвр* всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="70418-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="70418-110">Параметры *двдриверид*, *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="70418-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="70418-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70418-111">Return Value</span></span>

<span data-ttu-id="70418-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="70418-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="70418-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70418-113">Remarks</span></span>

<span data-ttu-id="70418-114">Сообщение **о \_ загрузке DRV** всегда является первым сообщением, которое получает драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="70418-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="70418-115">Требования</span><span class="sxs-lookup"><span data-stu-id="70418-115">Requirements</span></span>



| <span data-ttu-id="70418-116">Требование</span><span class="sxs-lookup"><span data-stu-id="70418-116">Requirement</span></span> | <span data-ttu-id="70418-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70418-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70418-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70418-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70418-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70418-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="70418-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70418-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70418-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70418-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="70418-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="70418-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70418-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70418-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70418-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70418-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70418-125">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="70418-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="70418-126">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="70418-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





