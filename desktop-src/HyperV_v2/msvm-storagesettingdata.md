---
description: Представляет параметры, относящиеся к хранению для виртуальной системы.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Класс Msvm_StorageSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651206"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="d819c-103">\_Класс мсвм сторажесеттингдата</span><span class="sxs-lookup"><span data-stu-id="d819c-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="d819c-104">Представляет параметры, относящиеся к хранению для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d819c-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="d819c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d819c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d819c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d819c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="d819c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d819c-107">Members</span></span>

<span data-ttu-id="d819c-108">Класс **мсвм \_ сторажесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d819c-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d819c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d819c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d819c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d819c-110">Properties</span></span>

<span data-ttu-id="d819c-111">Класс **мсвм \_ сторажесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d819c-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d819c-112">**дисаблеинтерруптбатчинг**</span><span class="sxs-lookup"><span data-stu-id="d819c-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d819c-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d819c-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d819c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d819c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d819c-115">Указывает, следует ли отключить пакетную обработку прерываний.</span><span class="sxs-lookup"><span data-stu-id="d819c-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="d819c-116">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="d819c-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d819c-117">**среадкаунтперчаннел**</span><span class="sxs-lookup"><span data-stu-id="d819c-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d819c-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d819c-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d819c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d819c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d819c-120">Количество потоков на канал хранилища для обработки операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="d819c-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="d819c-121">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d819c-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d819c-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="d819c-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d819c-123">Поведение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d819c-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="d819c-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкая** (1)</span><span class="sxs-lookup"><span data-stu-id="d819c-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d819c-125">Малое количество потоков на канал хранилища.</span><span class="sxs-lookup"><span data-stu-id="d819c-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="d819c-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Средний** (2)</span><span class="sxs-lookup"><span data-stu-id="d819c-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d819c-127">Среднее число потоков на канал хранилища.</span><span class="sxs-lookup"><span data-stu-id="d819c-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="d819c-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (3)</span><span class="sxs-lookup"><span data-stu-id="d819c-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d819c-129">Большое количество потоков на канал хранилища.</span><span class="sxs-lookup"><span data-stu-id="d819c-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d819c-130">**виртуалпроцессорсперчаннел**</span><span class="sxs-lookup"><span data-stu-id="d819c-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d819c-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d819c-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d819c-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d819c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d819c-133">Количество процессоров на канал хранилища.</span><span class="sxs-lookup"><span data-stu-id="d819c-133">The number of processors per storage channel.</span></span> <span data-ttu-id="d819c-134">Число открываемых каналов определяется (число логических процессоров на узле/**виртуалпроцессорсперчаннел**).</span><span class="sxs-lookup"><span data-stu-id="d819c-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="d819c-135">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d819c-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d819c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d819c-136">Requirements</span></span>



| <span data-ttu-id="d819c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="d819c-137">Requirement</span></span> | <span data-ttu-id="d819c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="d819c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d819c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d819c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d819c-140">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="d819c-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d819c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d819c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d819c-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d819c-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d819c-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d819c-143">Namespace</span></span><br/>                | <span data-ttu-id="d819c-144">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d819c-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d819c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d819c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d819c-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d819c-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d819c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d819c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d819c-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d819c-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d819c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d819c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d819c-150">**Мсвм \_ системкомпонентсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="d819c-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




