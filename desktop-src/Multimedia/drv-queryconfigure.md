---
title: Сообщение DRV_QUERYCONFIGURE (Ммсистем. h)
description: Указывает драйверу указать, поддерживает ли он пользовательскую конфигурацию.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262217"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="4f5c3-104">\_Куериконфигуре сообщение DRV</span><span class="sxs-lookup"><span data-stu-id="4f5c3-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="4f5c3-105">Указывает драйверу указать, поддерживает ли он пользовательскую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4f5c3-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f5c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f5c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f5c3-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="4f5c3-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="4f5c3-108">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="4f5c3-108">Identifier of the installable driver.</span></span> <span data-ttu-id="4f5c3-109">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="4f5c3-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="4f5c3-110"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="4f5c3-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="4f5c3-111">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="4f5c3-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f5c3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f5c3-112">Return Value</span></span>

<span data-ttu-id="4f5c3-113">Возвращает ненулевое значение, если драйвер может отображать диалоговое окно конфигурации или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4f5c3-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5c3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f5c3-114">Remarks</span></span>

<span data-ttu-id="4f5c3-115">Параметры *lParam1* и *lParam2* не используются.</span><span class="sxs-lookup"><span data-stu-id="4f5c3-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5c3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4f5c3-116">Requirements</span></span>



| <span data-ttu-id="4f5c3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4f5c3-117">Requirement</span></span> | <span data-ttu-id="4f5c3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4f5c3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5c3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f5c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5c3-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f5c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f5c3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f5c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5c3-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f5c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f5c3-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f5c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f5c3-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c3-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f5c3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f5c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5c3-126">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="4f5c3-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="4f5c3-127">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="4f5c3-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





