---
title: Сообщение DRV_ENABLE (Ммсистем. h)
description: Включает драйвер. Драйвер должен инициализировать любые переменные и выбрать устройства с интерфейсом ввода-вывода.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989357"
---
# <a name="drv_enable-message"></a><span data-ttu-id="e0831-105">DRV \_ включить сообщение</span><span class="sxs-lookup"><span data-stu-id="e0831-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="e0831-106">Включает драйвер.</span><span class="sxs-lookup"><span data-stu-id="e0831-106">Enables the driver.</span></span> <span data-ttu-id="e0831-107">Драйвер должен инициализировать любые переменные и выбрать устройства с интерфейсом ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e0831-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0831-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0831-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0831-109"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="e0831-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="e0831-110">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="e0831-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0831-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0831-111">Return Value</span></span>

<span data-ttu-id="e0831-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e0831-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0831-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0831-113">Remarks</span></span>

<span data-ttu-id="e0831-114">Параметры *двдриверид*, *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="e0831-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="e0831-115">Драйверы считаются включенными с момента получения этого сообщения, пока они не будут отключены с помощью сообщения об [**\_ отключении DRV**](drv-disable.md) .</span><span class="sxs-lookup"><span data-stu-id="e0831-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0831-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e0831-116">Requirements</span></span>



| <span data-ttu-id="e0831-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e0831-117">Requirement</span></span> | <span data-ttu-id="e0831-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0831-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0831-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0831-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0831-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e0831-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e0831-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0831-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0831-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e0831-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e0831-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e0831-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0831-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0831-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0831-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0831-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0831-126">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="e0831-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="e0831-127">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="e0831-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





