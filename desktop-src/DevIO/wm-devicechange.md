---
description: Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Сообщение WM_DEVICECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581506"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="0d45a-103">\_Сообщение ДЕВИЦЕЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="0d45a-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="0d45a-104">Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.</span><span class="sxs-lookup"><span data-stu-id="0d45a-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="0d45a-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0d45a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="0d45a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d45a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d45a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="0d45a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0d45a-108">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="0d45a-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="0d45a-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="0d45a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0d45a-110">Идентификатор **WM \_ девицечанже** .</span><span class="sxs-lookup"><span data-stu-id="0d45a-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0d45a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d45a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d45a-112">Произошедшее событие.</span><span class="sxs-lookup"><span data-stu-id="0d45a-112">The event that has occurred.</span></span> <span data-ttu-id="0d45a-113">Этот параметр может принимать одно из следующих значений из файла заголовка ДБТ. h.</span><span class="sxs-lookup"><span data-stu-id="0d45a-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="0d45a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0d45a-114">Value</span></span> | <span data-ttu-id="0d45a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d45a-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="0d45a-116">**[ДБТ \_ девнодес \_ изменен](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="0d45a-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="0d45a-117">0x0007</span></span> | <span data-ttu-id="0d45a-118">Устройство было добавлено в систему или удалено из нее.</span><span class="sxs-lookup"><span data-stu-id="0d45a-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="0d45a-119">**[ДБТ \_ куеричанжеконфиг](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="0d45a-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="0d45a-120">0x0017</span></span> | <span data-ttu-id="0d45a-121">Запрошено разрешение на изменение текущей конфигурации (закрепление или Отстыковка).</span><span class="sxs-lookup"><span data-stu-id="0d45a-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="0d45a-122">**[ДБТ \_ конфигчанжед](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="0d45a-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="0d45a-123">0x0018</span></span> | <span data-ttu-id="0d45a-124">Текущая конфигурация изменилась из-за закрепления или открепления.</span><span class="sxs-lookup"><span data-stu-id="0d45a-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="0d45a-125">**[ДБТ \_ конфигчанжеканцелед](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="0d45a-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="0d45a-126">0x0019</span></span> | <span data-ttu-id="0d45a-127">Запрос на изменение текущей конфигурации (закрепления или отстыковки) отменен.</span><span class="sxs-lookup"><span data-stu-id="0d45a-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="0d45a-128">**[ДБТ \_ девицеарривал](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="0d45a-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="0d45a-129">0x8000</span></span> | <span data-ttu-id="0d45a-130">Устройство или носитель вставлены и теперь доступны.</span><span class="sxs-lookup"><span data-stu-id="0d45a-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="0d45a-131">**[ДБТ \_ девицекуериремове](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="0d45a-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="0d45a-132">0x8001</span></span> | <span data-ttu-id="0d45a-133">Запрошено разрешение на удаление устройства или фрагмента носителя.</span><span class="sxs-lookup"><span data-stu-id="0d45a-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="0d45a-134">Любое приложение может отклонить этот запрос и отменить удаление.</span><span class="sxs-lookup"><span data-stu-id="0d45a-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="0d45a-135">**[ДБТ \_ девицекуериремовефаилед](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="0d45a-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="0d45a-136">0x8002</span></span> | <span data-ttu-id="0d45a-137">Запрос на удаление устройства или носителя был отменен.</span><span class="sxs-lookup"><span data-stu-id="0d45a-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="0d45a-138">**[ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="0d45a-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="0d45a-139">0x8003</span></span> | <span data-ttu-id="0d45a-140">Устройство или носитель будет удален.</span><span class="sxs-lookup"><span data-stu-id="0d45a-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="0d45a-141">Нельзя запретить.</span><span class="sxs-lookup"><span data-stu-id="0d45a-141">Cannot be denied.</span></span> |
| <span data-ttu-id="0d45a-142">**[ДБТ \_ девицеремовекомплете](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="0d45a-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="0d45a-143">0x8004</span></span> | <span data-ttu-id="0d45a-144">Устройство или носитель с носителем были удалены.</span><span class="sxs-lookup"><span data-stu-id="0d45a-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="0d45a-145">**[ДБТ \_ девицетипеспеЦифик](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="0d45a-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="0d45a-146">0x8005</span></span> | <span data-ttu-id="0d45a-147">Произошло событие для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="0d45a-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="0d45a-148">**[ДБТ \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="0d45a-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="0d45a-149">0x8006</span></span> | <span data-ttu-id="0d45a-150">Произошло пользовательское событие.</span><span class="sxs-lookup"><span data-stu-id="0d45a-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="0d45a-151">**[ДБТ \_ пользователяопределенные](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="0d45a-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="0d45a-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="0d45a-152">0xFFFF</span></span> | <span data-ttu-id="0d45a-153">Значение этого сообщения определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="0d45a-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="0d45a-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d45a-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d45a-155">Указатель на структуру, содержащую данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="0d45a-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="0d45a-156">Его формат зависит от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0d45a-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="0d45a-157">Дополнительные сведения см. в документации по каждому событию.</span><span class="sxs-lookup"><span data-stu-id="0d45a-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d45a-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d45a-158">Return value</span></span>

<span data-ttu-id="0d45a-159">Возвращает **значение true** , чтобы предоставить запрос.</span><span class="sxs-lookup"><span data-stu-id="0d45a-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="0d45a-160">Верните **широковещательный \_ запрос \_ Deny** , чтобы отклонить запрос.</span><span class="sxs-lookup"><span data-stu-id="0d45a-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d45a-161">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d45a-161">Remarks</span></span>

<span data-ttu-id="0d45a-162">Для устройств, которые предлагают функции, управляемые программным обеспечением, такие как извлечение и блокировка, система обычно отправляет сообщение [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) , чтобы позволить приложениям и драйверам устройств правильно использовать устройство.</span><span class="sxs-lookup"><span data-stu-id="0d45a-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="0d45a-163">Если система принудительно удаляет устройство, оно может не отправить сообщение [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) перед этим.</span><span class="sxs-lookup"><span data-stu-id="0d45a-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d45a-164">Требования</span><span class="sxs-lookup"><span data-stu-id="0d45a-164">Requirements</span></span>

| <span data-ttu-id="0d45a-165">Требование</span><span class="sxs-lookup"><span data-stu-id="0d45a-165">Requirement</span></span> | <span data-ttu-id="0d45a-166">Значение</span><span class="sxs-lookup"><span data-stu-id="0d45a-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d45a-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d45a-167">Minimum supported client</span></span> | <span data-ttu-id="0d45a-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d45a-168">Windows XP</span></span> |
| <span data-ttu-id="0d45a-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d45a-169">Minimum supported server</span></span> | <span data-ttu-id="0d45a-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d45a-170">Windows Server 2003</span></span>|
| <span data-ttu-id="0d45a-171">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0d45a-171">Header</span></span> | <dl> <span data-ttu-id="0d45a-172"><dt>Winuser. h (включая Windows. h или ДБТ. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d45a-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="0d45a-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d45a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d45a-174">ДБТ \_ конфигчанжеканцелед</span><span class="sxs-lookup"><span data-stu-id="0d45a-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="0d45a-175">ДБТ \_ конфигчанжед</span><span class="sxs-lookup"><span data-stu-id="0d45a-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="0d45a-176">ДБТ \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="0d45a-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="0d45a-177">ДБТ \_ девицеарривал</span><span class="sxs-lookup"><span data-stu-id="0d45a-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="0d45a-178">ДБТ \_ девицекуериремове</span><span class="sxs-lookup"><span data-stu-id="0d45a-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="0d45a-179">ДБТ \_ девицекуериремовефаилед</span><span class="sxs-lookup"><span data-stu-id="0d45a-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="0d45a-180">ДБТ \_ девицеремовекомплете</span><span class="sxs-lookup"><span data-stu-id="0d45a-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="0d45a-181">ДБТ \_ девицеремовепендинг</span><span class="sxs-lookup"><span data-stu-id="0d45a-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="0d45a-182">ДБТ \_ девицетипеспеЦифик</span><span class="sxs-lookup"><span data-stu-id="0d45a-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="0d45a-183">ДБТ \_ девнодес \_ изменен</span><span class="sxs-lookup"><span data-stu-id="0d45a-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="0d45a-184">ДБТ \_ куеричанжеконфиг</span><span class="sxs-lookup"><span data-stu-id="0d45a-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="0d45a-185">ДБТ \_ пользователяопределенные</span><span class="sxs-lookup"><span data-stu-id="0d45a-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>
