---
title: Сообщение DRV_INSTALL (Ммсистем. h)
description: Уведомляет устанавливаемый драйвер. Драйвер должен создать и инициализировать все необходимые разделы и значения реестра, а также убедиться, что вспомогательные драйверы и оборудование установлены и правильно настроены.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989353"
---
# <a name="drv_install-message"></a><span data-ttu-id="3115f-105">\_Сообщение об установке DRV</span><span class="sxs-lookup"><span data-stu-id="3115f-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="3115f-106">Уведомляет устанавливаемый драйвер.</span><span class="sxs-lookup"><span data-stu-id="3115f-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="3115f-107">Драйвер должен создать и инициализировать все необходимые разделы и значения реестра, а также убедиться, что вспомогательные драйверы и оборудование установлены и правильно настроены.</span><span class="sxs-lookup"><span data-stu-id="3115f-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="3115f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3115f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3115f-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="3115f-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="3115f-110">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="3115f-110">Identifier of the installable driver.</span></span> <span data-ttu-id="3115f-111">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="3115f-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="3115f-112"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="3115f-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="3115f-113">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="3115f-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="3115f-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3115f-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3115f-115">Адрес структуры [**дрвконфигинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3115f-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="3115f-116">Если задана структура, она содержит имена раздела реестра и значения, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="3115f-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3115f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3115f-117">Return Value</span></span>

<span data-ttu-id="3115f-118">Возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3115f-118">Returns one of these values:</span></span>



| <span data-ttu-id="3115f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3115f-119">Requirement</span></span> | <span data-ttu-id="3115f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3115f-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3115f-121">ДРВКНФ \_ ОК</span><span class="sxs-lookup"><span data-stu-id="3115f-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="3115f-122">Установка выполнена успешно; дальнейшие действия не требуются.</span><span class="sxs-lookup"><span data-stu-id="3115f-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="3115f-123">ДРВКНФ \_ Отмена</span><span class="sxs-lookup"><span data-stu-id="3115f-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="3115f-124">Сбой установки..</span><span class="sxs-lookup"><span data-stu-id="3115f-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="3115f-125">перезапустить ДРВКНФ \_</span><span class="sxs-lookup"><span data-stu-id="3115f-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="3115f-126">Установка выполнена успешно, но она вступит в силу только после перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="3115f-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3115f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3115f-127">Remarks</span></span>

<span data-ttu-id="3115f-128">Параметр *lParam1* не используется.</span><span class="sxs-lookup"><span data-stu-id="3115f-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="3115f-129">Некоторые устанавливаемые драйверы добавляют сведения о конфигурации к значению, назначенному значению реестра, связанному с драйвером.</span><span class="sxs-lookup"><span data-stu-id="3115f-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3115f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3115f-130">Requirements</span></span>



| <span data-ttu-id="3115f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3115f-131">Requirement</span></span> | <span data-ttu-id="3115f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3115f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3115f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3115f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3115f-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3115f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3115f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3115f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3115f-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3115f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3115f-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3115f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3115f-138"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3115f-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3115f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3115f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3115f-140">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="3115f-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="3115f-141">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="3115f-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

