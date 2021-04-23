---
title: Сообщение DRV_DISABLE (Ммсистем. h)
description: Отключает драйвер. Драйвер должен разместить соответствующее устройство (если оно имеется) в неактивном состоянии и завершить любые функции обратного вызова или потоки.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989355"
---
# <a name="drv_disable-message"></a><span data-ttu-id="2112a-105">DRV \_ отключить сообщение</span><span class="sxs-lookup"><span data-stu-id="2112a-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="2112a-106">Отключает драйвер.</span><span class="sxs-lookup"><span data-stu-id="2112a-106">Disables the driver.</span></span> <span data-ttu-id="2112a-107">Драйвер должен разместить соответствующее устройство (если оно имеется) в неактивном состоянии и завершить любые функции обратного вызова или потоки.</span><span class="sxs-lookup"><span data-stu-id="2112a-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="2112a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2112a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2112a-109"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="2112a-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="2112a-110">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="2112a-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2112a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2112a-111">Return Value</span></span>

<span data-ttu-id="2112a-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2112a-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2112a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2112a-113">Remarks</span></span>

<span data-ttu-id="2112a-114">Параметры *двдриверид*, *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="2112a-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="2112a-115">После отключения драйвера система обычно отправляет драйверу краткое сообщение [**DRV \_**](drv-free.md) , прежде чем удалить драйвер из памяти.</span><span class="sxs-lookup"><span data-stu-id="2112a-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="2112a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2112a-116">Requirements</span></span>



| <span data-ttu-id="2112a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2112a-117">Requirement</span></span> | <span data-ttu-id="2112a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2112a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2112a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2112a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2112a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2112a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2112a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2112a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2112a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2112a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2112a-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2112a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2112a-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2112a-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2112a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2112a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2112a-126">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="2112a-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="2112a-127">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="2112a-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





