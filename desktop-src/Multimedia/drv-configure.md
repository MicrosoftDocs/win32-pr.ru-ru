---
title: Сообщение DRV_CONFIGURE (Ммсистем. h)
description: Указывает, что устанавливаемый драйвер отображает диалоговое окно конфигурации и позволяет пользователю указать новые параметры для данного устанавливаемого экземпляра драйвера.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989356"
---
# <a name="drv_configure-message"></a><span data-ttu-id="2c58e-104">DRV \_ Настройка сообщения</span><span class="sxs-lookup"><span data-stu-id="2c58e-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="2c58e-105">Указывает, что устанавливаемый драйвер отображает диалоговое окно конфигурации и позволяет пользователю указать новые параметры для данного устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="2c58e-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c58e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c58e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c58e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="2c58e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="2c58e-108">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="2c58e-108">Identifier of the installable driver.</span></span> <span data-ttu-id="2c58e-109">Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="2c58e-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="2c58e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="2c58e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="2c58e-111">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="2c58e-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="2c58e-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2c58e-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2c58e-113">Маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="2c58e-113">Handle of the parent window.</span></span> <span data-ttu-id="2c58e-114">Это окно используется в качестве родительского окна для диалогового окна Конфигурация.</span><span class="sxs-lookup"><span data-stu-id="2c58e-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2c58e-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2c58e-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2c58e-116">Адрес структуры [**дрвконфигинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2c58e-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="2c58e-117">Если задана структура, она содержит имена раздела реестра и значения, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="2c58e-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c58e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c58e-118">Return Value</span></span>

<span data-ttu-id="2c58e-119">Возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2c58e-119">Returns one of these values:</span></span>



| <span data-ttu-id="2c58e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2c58e-120">Requirement</span></span> | <span data-ttu-id="2c58e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2c58e-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c58e-122">ДРВКНФ \_ ОК</span><span class="sxs-lookup"><span data-stu-id="2c58e-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="2c58e-123">Конфигурация успешно выполнена; дальнейшие действия не требуются.</span><span class="sxs-lookup"><span data-stu-id="2c58e-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="2c58e-124">ДРВКНФ \_ Отмена</span><span class="sxs-lookup"><span data-stu-id="2c58e-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="2c58e-125">Пользователь отменил это диалоговое окно; дальнейшие действия не требуются.</span><span class="sxs-lookup"><span data-stu-id="2c58e-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="2c58e-126">перезапустить ДРВКНФ \_</span><span class="sxs-lookup"><span data-stu-id="2c58e-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="2c58e-127">Настройка прошла успешно, но изменения вступят в силу только после перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="2c58e-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2c58e-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c58e-128">Remarks</span></span>

<span data-ttu-id="2c58e-129">Некоторые устанавливаемые драйверы добавляют сведения о конфигурации к значению, назначенному значению реестра, связанному с драйвером.</span><span class="sxs-lookup"><span data-stu-id="2c58e-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="2c58e-130">\_Возвращаемые значения DRV Cancel, DRV \_ ОК и DRV \_ устарели. они заменены на ДРВКНФ \_ Cancel, дрвкнф \_ ОК и дрвкнф \_ restart соответственно.</span><span class="sxs-lookup"><span data-stu-id="2c58e-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c58e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="2c58e-131">Requirements</span></span>



| <span data-ttu-id="2c58e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="2c58e-132">Requirement</span></span> | <span data-ttu-id="2c58e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2c58e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c58e-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c58e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2c58e-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c58e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c58e-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c58e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2c58e-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c58e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2c58e-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c58e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c58e-139"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c58e-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c58e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c58e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c58e-141">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="2c58e-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="2c58e-142">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="2c58e-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

