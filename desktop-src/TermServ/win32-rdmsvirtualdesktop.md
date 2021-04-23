---
title: Класс Win32_RDMSVirtualDesktop
description: Представляет виртуальный рабочий стол.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSVirtualDesktop, описание
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672614"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="92245-105">\_Класс Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="92245-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="92245-106">Представляет виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="92245-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="92245-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="92245-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92245-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92245-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="92245-109">Члены</span><span class="sxs-lookup"><span data-stu-id="92245-109">Members</span></span>

<span data-ttu-id="92245-110">Класс **Win32 \_ рдмсвиртуалдесктоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92245-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="92245-111">Методы</span><span class="sxs-lookup"><span data-stu-id="92245-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="92245-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="92245-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92245-113">Методы</span><span class="sxs-lookup"><span data-stu-id="92245-113">Methods</span></span>

<span data-ttu-id="92245-114">Класс **Win32 \_ рдмсвиртуалдесктоп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="92245-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="92245-115">Метод</span><span class="sxs-lookup"><span data-stu-id="92245-115">Method</span></span>                                                                                              | <span data-ttu-id="92245-116">Описание</span><span class="sxs-lookup"><span data-stu-id="92245-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92245-117">**жетусерассигнмент**</span><span class="sxs-lookup"><span data-stu-id="92245-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="92245-118">Получение имени пользователя и домена пользователя, назначенного виртуальному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="92245-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="92245-119">**жетвиртуалдесктопассигнедтаусер**</span><span class="sxs-lookup"><span data-stu-id="92245-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="92245-120">Извлекает виртуальный рабочий стол, назначенный указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="92245-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="92245-121">**жетвиртуалдесктопдетаилс**</span><span class="sxs-lookup"><span data-stu-id="92245-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="92245-122">Получение дополнительных сведений о виртуальном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="92245-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="92245-123">**жетвиртуалдесктопстате**</span><span class="sxs-lookup"><span data-stu-id="92245-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="92245-124">Получает состояние виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="92245-125">**ремовеусерассигнмент**</span><span class="sxs-lookup"><span data-stu-id="92245-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="92245-126">Удаляет назначение пользователя из виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="92245-127">**сетусерассигнмент**</span><span class="sxs-lookup"><span data-stu-id="92245-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="92245-128">Назначает пользователю виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="92245-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="92245-129">**сетвиртуалдесктопстате**</span><span class="sxs-lookup"><span data-stu-id="92245-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="92245-130">Обновляет состояние виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="92245-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="92245-131">Properties</span></span>

<span data-ttu-id="92245-132">Класс **Win32 \_ рдмсвиртуалдесктоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92245-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92245-133">**коллектионалиас**</span><span class="sxs-lookup"><span data-stu-id="92245-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-136">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92245-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92245-137">Возвращает псевдоним коллекции виртуальных рабочих столов, которая управляет виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="92245-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="92245-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="92245-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92245-141">Возвращает имя компьютера, на котором размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="92245-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="92245-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="92245-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92245-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92245-146">Возвращает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92245-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="92245-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="92245-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-150">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92245-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92245-151">Возвращает состояние сеанса виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="92245-152">**сессионусернаме**</span><span class="sxs-lookup"><span data-stu-id="92245-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-155">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92245-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92245-156">Возвращает имя пользователя, выполнившего вход в сеанс виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="92245-157">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="92245-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92245-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92245-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92245-160">Возвращает состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92245-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="92245-161">**Доменпользователя**</span><span class="sxs-lookup"><span data-stu-id="92245-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-164">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92245-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92245-165">Возвращает доменное имя пользователя, назначенного виртуальному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="92245-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="92245-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="92245-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92245-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92245-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92245-169">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92245-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92245-170">Возвращает имя пользователя, назначенного виртуальному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="92245-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="92245-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="92245-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92245-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92245-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92245-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92245-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92245-174">Возвращает состояние виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="92245-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92245-175">Требования</span><span class="sxs-lookup"><span data-stu-id="92245-175">Requirements</span></span>



| <span data-ttu-id="92245-176">Требование</span><span class="sxs-lookup"><span data-stu-id="92245-176">Requirement</span></span> | <span data-ttu-id="92245-177">Значение</span><span class="sxs-lookup"><span data-stu-id="92245-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="92245-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92245-178">Minimum supported client</span></span><br/> | <span data-ttu-id="92245-179">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92245-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="92245-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92245-180">Minimum supported server</span></span><br/> | <span data-ttu-id="92245-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92245-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="92245-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92245-182">Namespace</span></span><br/>                | <span data-ttu-id="92245-183">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="92245-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="92245-184">MOF</span><span class="sxs-lookup"><span data-stu-id="92245-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92245-185"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92245-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="92245-186">DLL</span><span class="sxs-lookup"><span data-stu-id="92245-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92245-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92245-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="92245-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92245-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92245-189">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="92245-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

