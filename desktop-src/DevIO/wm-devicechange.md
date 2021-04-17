---
description: Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Сообщение WM_DEVICECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423297"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="bb108-103">\_Сообщение ДЕВИЦЕЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="bb108-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="bb108-104">Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.</span><span class="sxs-lookup"><span data-stu-id="bb108-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="bb108-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bb108-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="bb108-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb108-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb108-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bb108-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bb108-108">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="bb108-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bb108-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="bb108-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bb108-110">Идентификатор **WM \_ девицечанже** .</span><span class="sxs-lookup"><span data-stu-id="bb108-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bb108-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb108-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb108-112">Произошедшее событие.</span><span class="sxs-lookup"><span data-stu-id="bb108-112">The event that has occurred.</span></span> <span data-ttu-id="bb108-113">Этот параметр может принимать одно из следующих значений из файла заголовка ДБТ. h.</span><span class="sxs-lookup"><span data-stu-id="bb108-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="bb108-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bb108-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="bb108-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bb108-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="bb108-116"><dt>**[ДБТ \_ КОНФИГЧАНЖЕКАНЦЕЛЕД](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="bb108-117">Запрос на изменение текущей конфигурации (закрепления или отстыковки) отменен.</span><span class="sxs-lookup"><span data-stu-id="bb108-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="bb108-118"><dt>**[ДБТ \_ КОНФИГЧАНЖЕД](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="bb108-119">Текущая конфигурация изменилась из-за закрепления или открепления.</span><span class="sxs-lookup"><span data-stu-id="bb108-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="bb108-120"><dt>**[ДБТ \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="bb108-121">Произошло пользовательское событие.</span><span class="sxs-lookup"><span data-stu-id="bb108-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="bb108-122"><dt>**[ДБТ \_ ДЕВИЦЕАРРИВАЛ](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="bb108-123">Устройство или носитель вставлены и теперь доступны.</span><span class="sxs-lookup"><span data-stu-id="bb108-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="bb108-124"><dt>**[ДБТ \_ ДЕВИЦЕКУЕРИРЕМОВЕ](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="bb108-125">Запрошено разрешение на удаление устройства или фрагмента носителя.</span><span class="sxs-lookup"><span data-stu-id="bb108-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="bb108-126">Любое приложение может отклонить этот запрос и отменить удаление.</span><span class="sxs-lookup"><span data-stu-id="bb108-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="bb108-127"><dt>**[ДБТ \_ ДЕВИЦЕКУЕРИРЕМОВЕФАИЛЕД](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="bb108-128">Запрос на удаление устройства или носителя был отменен.</span><span class="sxs-lookup"><span data-stu-id="bb108-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="bb108-129"><dt>**[ДБТ \_ ДЕВИЦЕРЕМОВЕКОМПЛЕТЕ](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="bb108-130">Устройство или носитель с носителем были удалены.</span><span class="sxs-lookup"><span data-stu-id="bb108-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="bb108-131"><dt>**[ДБТ \_ ДЕВИЦЕРЕМОВЕПЕНДИНГ](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="bb108-132">Устройство или носитель будет удален.</span><span class="sxs-lookup"><span data-stu-id="bb108-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="bb108-133">Нельзя запретить.</span><span class="sxs-lookup"><span data-stu-id="bb108-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="bb108-134"><dt>**[ДБТ \_ ДЕВИЦЕТИПЕСПЕЦИФИК](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="bb108-135">Произошло событие для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="bb108-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="bb108-136"><dt>**[ДБТ \_ ДЕВНОДЕС \_ изменил](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="bb108-137">Устройство было добавлено в систему или удалено из нее.</span><span class="sxs-lookup"><span data-stu-id="bb108-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="bb108-138"><dt>**[ДБТ \_ КУЕРИЧАНЖЕКОНФИГ](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="bb108-139">Запрошено разрешение на изменение текущей конфигурации (закрепление или Отстыковка).</span><span class="sxs-lookup"><span data-stu-id="bb108-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="bb108-140"><dt>**[ДБТ \_ ПОЛЬЗОВАТЕЛЯОПРЕДЕЛЕННЫЕ](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="bb108-141">Значение этого сообщения определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="bb108-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="bb108-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb108-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb108-143">Указатель на структуру, содержащую данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="bb108-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="bb108-144">Его формат зависит от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="bb108-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="bb108-145">Дополнительные сведения см. в документации по каждому событию.</span><span class="sxs-lookup"><span data-stu-id="bb108-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb108-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb108-146">Return value</span></span>

<span data-ttu-id="bb108-147">Возвращает **значение true** , чтобы предоставить запрос.</span><span class="sxs-lookup"><span data-stu-id="bb108-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="bb108-148">Верните **широковещательный \_ запрос \_ Deny** , чтобы отклонить запрос.</span><span class="sxs-lookup"><span data-stu-id="bb108-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb108-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb108-149">Remarks</span></span>

<span data-ttu-id="bb108-150">Для устройств, которые предлагают функции, управляемые программным обеспечением, такие как извлечение и блокировка, система обычно отправляет сообщение [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) , чтобы позволить приложениям и драйверам устройств правильно использовать устройство.</span><span class="sxs-lookup"><span data-stu-id="bb108-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="bb108-151">Если система принудительно удаляет устройство, оно может не отправить сообщение [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) перед этим.</span><span class="sxs-lookup"><span data-stu-id="bb108-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb108-152">Требования</span><span class="sxs-lookup"><span data-stu-id="bb108-152">Requirements</span></span>



| <span data-ttu-id="bb108-153">Требование</span><span class="sxs-lookup"><span data-stu-id="bb108-153">Requirement</span></span> | <span data-ttu-id="bb108-154">Значение</span><span class="sxs-lookup"><span data-stu-id="bb108-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb108-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb108-155">Minimum supported client</span></span><br/> | <span data-ttu-id="bb108-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb108-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="bb108-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb108-157">Minimum supported server</span></span><br/> | <span data-ttu-id="bb108-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb108-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="bb108-159">Header</span><span class="sxs-lookup"><span data-stu-id="bb108-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb108-160"><dt>Winuser. h (включая Windows. h или ДБТ. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb108-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb108-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb108-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb108-162">ДБТ \_ конфигчанжеканцелед</span><span class="sxs-lookup"><span data-stu-id="bb108-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="bb108-163">ДБТ \_ конфигчанжед</span><span class="sxs-lookup"><span data-stu-id="bb108-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="bb108-164">ДБТ \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="bb108-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="bb108-165">ДБТ \_ девицеарривал</span><span class="sxs-lookup"><span data-stu-id="bb108-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="bb108-166">ДБТ \_ девицекуериремове</span><span class="sxs-lookup"><span data-stu-id="bb108-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="bb108-167">ДБТ \_ девицекуериремовефаилед</span><span class="sxs-lookup"><span data-stu-id="bb108-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="bb108-168">ДБТ \_ девицеремовекомплете</span><span class="sxs-lookup"><span data-stu-id="bb108-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="bb108-169">ДБТ \_ девицеремовепендинг</span><span class="sxs-lookup"><span data-stu-id="bb108-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="bb108-170">ДБТ \_ девицетипеспеЦифик</span><span class="sxs-lookup"><span data-stu-id="bb108-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="bb108-171">ДБТ \_ девнодес \_ изменен</span><span class="sxs-lookup"><span data-stu-id="bb108-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="bb108-172">ДБТ \_ куеричанжеконфиг</span><span class="sxs-lookup"><span data-stu-id="bb108-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="bb108-173">ДБТ \_ пользователяопределенные</span><span class="sxs-lookup"><span data-stu-id="bb108-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 

