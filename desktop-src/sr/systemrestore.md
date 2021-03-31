---
title: Класс SystemRestore
description: Предоставляет методы для отключения и включения мониторинга, перечисления доступных точек восстановления и инициации восстановления в локальной системе.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Восстановление системы класса SystemRestore
- Восстановление системы класса SystemRestore, описание
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071747"
---
# <a name="systemrestore-class"></a><span data-ttu-id="6e5a5-105">Класс SystemRestore</span><span class="sxs-lookup"><span data-stu-id="6e5a5-105">SystemRestore class</span></span>

<span data-ttu-id="6e5a5-106">Предоставляет методы для отключения и включения мониторинга, перечисления доступных точек восстановления и инициации восстановления в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e5a5-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="6e5a5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6e5a5-108">Members</span></span>

<span data-ttu-id="6e5a5-109">Класс **SystemRestore** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6e5a5-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="6e5a5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6e5a5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6e5a5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e5a5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6e5a5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6e5a5-112">Methods</span></span>

<span data-ttu-id="6e5a5-113">Класс **SystemRestore** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="6e5a5-114">Метод</span><span class="sxs-lookup"><span data-stu-id="6e5a5-114">Method</span></span>                                                             | <span data-ttu-id="6e5a5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6e5a5-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="6e5a5-116">**креатересторепоинт**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="6e5a5-117">Создает точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="6e5a5-118">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="6e5a5-119">Отключает мониторинг на определенном диске.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="6e5a5-120">**Включить**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="6e5a5-121">Включает наблюдение на определенном диске.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="6e5a5-122">**жетластресторестатус**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="6e5a5-123">Возвращает состояние последнего восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="6e5a5-124">**Восстановлен**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="6e5a5-125">Инициирует восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="6e5a5-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e5a5-126">Properties</span></span>

<span data-ttu-id="6e5a5-127">Класс **SystemRestore** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e5a5-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5a5-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e5a5-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6e5a5-131">Время, когда произошло изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6e5a5-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5a5-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e5a5-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6e5a5-135">Отображаемое описание, чтобы пользователь мог легко найти точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="6e5a5-136">Максимальная длина строки ANSI — MAX \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="6e5a5-137">Максимальная длина строки Юникода — MAX \_ DESC \_ W.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="6e5a5-138">Дополнительные сведения см. в разделе [текст описания точки восстановления](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="6e5a5-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e5a5-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5a5-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e5a5-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6e5a5-142">Тип события.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-142">The type of event.</span></span> <span data-ttu-id="6e5a5-143">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="6e5a5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5a5-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="6e5a5-145">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5a5-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="6e5a5-146"><dt>**Начало \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="6e5a5-147">Начато изменение системы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-147">A system change has begun.</span></span> <span data-ttu-id="6e5a5-148">Последующий вложенный вызов не создает новую точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="6e5a5-149">Последующие вызовы должны использовать КОНЕЧные \_ вложенные \_ \_ изменения системы, а не конечные \_ \_ изменения системы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="6e5a5-150"><dt>**Начало \_ \_Изменение системы**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="6e5a5-151">Начато изменение системы.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="6e5a5-152"><dt>**Конец \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="6e5a5-153">Изменение системы завершено.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="6e5a5-154"><dt>**Конец \_ \_Изменение системы**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="6e5a5-155">Изменение системы завершено.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="6e5a5-156">**ресторепоинттипе**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5a5-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e5a5-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6e5a5-159">Тип точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-159">The type of restore point.</span></span> <span data-ttu-id="6e5a5-160">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="6e5a5-161">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5a5-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="6e5a5-162">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5a5-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="6e5a5-163"><dt>**Приложение \_ УСТАНОВИТЬ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="6e5a5-164">Приложение установлено.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="6e5a5-165"><dt>**Приложение \_ Удаление**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="6e5a5-166">Удалено приложение.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="6e5a5-167"><dt>**Отменено \_ Операция**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="6e5a5-168">Приложению необходимо удалить созданную точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="6e5a5-169">Например, приложение будет использовать этот флаг, когда пользователь отменит установку.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="6e5a5-170"><dt>**Устройство \_ \_Установка драйвера**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="6e5a5-171">Установлен драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="6e5a5-172"><dt>**Изменение \_ Параметры**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="6e5a5-173">В приложении были добавлены или удалены компоненты.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6e5a5-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5a5-175">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e5a5-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6e5a5-177">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="6e5a5-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6e5a5-178">Порядковый номер точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e5a5-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e5a5-179">Remarks</span></span>

<span data-ttu-id="6e5a5-180">Список точек восстановления можно получить с помощью метода [**SwbemServices. инстанцесоф**](/windows/desktop/WmiSdk/swbemservices-instancesof) , чтобы получить коллекцию объектов **SystemRestore** .</span><span class="sxs-lookup"><span data-stu-id="6e5a5-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="6e5a5-181">Для указания точки восстановления можно использовать свойства класса.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="6e5a5-182">Примеры</span><span class="sxs-lookup"><span data-stu-id="6e5a5-182">Examples</span></span>

<span data-ttu-id="6e5a5-183">Следующий пример скрипта перечисляет текущие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="6e5a5-184">Требования</span><span class="sxs-lookup"><span data-stu-id="6e5a5-184">Requirements</span></span>



| <span data-ttu-id="6e5a5-185">Требование</span><span class="sxs-lookup"><span data-stu-id="6e5a5-185">Requirement</span></span> | <span data-ttu-id="6e5a5-186">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5a5-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6e5a5-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e5a5-187">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5a5-188">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e5a5-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6e5a5-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e5a5-189">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5a5-190">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6e5a5-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="6e5a5-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e5a5-191">Namespace</span></span><br/>                | <span data-ttu-id="6e5a5-192">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6e5a5-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="6e5a5-193">MOF</span><span class="sxs-lookup"><span data-stu-id="6e5a5-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e5a5-194"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a5-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5a5-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e5a5-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5a5-196">Инструментарий управления Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="6e5a5-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

