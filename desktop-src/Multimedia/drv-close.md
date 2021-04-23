---
title: Сообщение DRV_CLOSE (Ммсистем. h)
description: Указывает драйверу закрыть заданный экземпляр. Если другие экземпляры не открыты, драйвер должен подготовиться к последующему выпуску из памяти.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650398"
---
# <a name="drv_close-message"></a><span data-ttu-id="664eb-105">\_Сообщение о закрытии DRV</span><span class="sxs-lookup"><span data-stu-id="664eb-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="664eb-106">Указывает драйверу закрыть заданный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="664eb-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="664eb-107">Если другие экземпляры не открыты, драйвер должен подготовиться к последующему выпуску из памяти.</span><span class="sxs-lookup"><span data-stu-id="664eb-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="664eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="664eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="664eb-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="664eb-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="664eb-110">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="664eb-110">Identifier of the installable driver.</span></span> <span data-ttu-id="664eb-111">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="664eb-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-112"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="664eb-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="664eb-113">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="664eb-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="664eb-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="664eb-115">32-разрядное значение, заданное в качестве параметра *lParam1* в вызове функции **дриверклосе** .</span><span class="sxs-lookup"><span data-stu-id="664eb-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="664eb-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="664eb-117">32-разрядное значение, заданное в качестве параметра *lParam2* в вызове функции **дриверклосе** .</span><span class="sxs-lookup"><span data-stu-id="664eb-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="664eb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="664eb-118">Return Value</span></span>

<span data-ttu-id="664eb-119">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="664eb-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="664eb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="664eb-120">Requirements</span></span>



| <span data-ttu-id="664eb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="664eb-121">Requirement</span></span> | <span data-ttu-id="664eb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="664eb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="664eb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="664eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="664eb-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="664eb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="664eb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="664eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="664eb-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="664eb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="664eb-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="664eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="664eb-128"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="664eb-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664eb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="664eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664eb-130">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="664eb-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="664eb-131">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="664eb-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





