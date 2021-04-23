---
description: Представляет параметры яркости монитора компьютера.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Класс Вмимониторбригхтнесс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703021"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="f1beb-103">Класс Вмимониторбригхтнесс</span><span class="sxs-lookup"><span data-stu-id="f1beb-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="f1beb-104">Класс WMI **вмимониторбригхтнесс** представляет параметры яркости монитора компьютера.</span><span class="sxs-lookup"><span data-stu-id="f1beb-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1beb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1beb-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="f1beb-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f1beb-106">Members</span></span>

<span data-ttu-id="f1beb-107">Класс **вмимониторбригхтнесс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f1beb-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="f1beb-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1beb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1beb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1beb-109">Properties</span></span>

<span data-ttu-id="f1beb-110">Класс **вмимониторбригхтнесс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f1beb-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1beb-111">**Активен**</span><span class="sxs-lookup"><span data-stu-id="f1beb-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1beb-112">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1beb-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1beb-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1beb-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1beb-114">Указывает, активен ли целевой монитор.</span><span class="sxs-lookup"><span data-stu-id="f1beb-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="f1beb-115">**куррентбригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="f1beb-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1beb-116">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f1beb-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f1beb-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1beb-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1beb-118">Текущая яркость.</span><span class="sxs-lookup"><span data-stu-id="f1beb-118">Current brightness.</span></span> <span data-ttu-id="f1beb-119">Это значение должно быть значением, взятым из *уровней*.</span><span class="sxs-lookup"><span data-stu-id="f1beb-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="f1beb-120">Пример: 100</span><span class="sxs-lookup"><span data-stu-id="f1beb-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="f1beb-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="f1beb-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1beb-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1beb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1beb-123">Квалификаторы: ключ</span><span class="sxs-lookup"><span data-stu-id="f1beb-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="f1beb-124">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="f1beb-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="f1beb-125">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="f1beb-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1beb-126">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f1beb-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f1beb-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1beb-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1beb-128">Массив, содержащий возможные уровни яркости.</span><span class="sxs-lookup"><span data-stu-id="f1beb-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="f1beb-129">Пример: \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="f1beb-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="f1beb-130">**Уровни**</span><span class="sxs-lookup"><span data-stu-id="f1beb-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1beb-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1beb-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1beb-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1beb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1beb-133">Общее число уровней яркости, поддерживаемых монитором, как описано в разделе *уровень*.</span><span class="sxs-lookup"><span data-stu-id="f1beb-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="f1beb-134">Пример: 101</span><span class="sxs-lookup"><span data-stu-id="f1beb-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f1beb-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="f1beb-135">Examples</span></span>

<span data-ttu-id="f1beb-136">Дополнительные сведения и примеры кода по использованию этого класса в PowerShell см. в разделе [Использование PowerShell для сообщения и Установка яркости монитора](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1beb-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1beb-137">Требования</span><span class="sxs-lookup"><span data-stu-id="f1beb-137">Requirements</span></span>



| <span data-ttu-id="f1beb-138">Требование</span><span class="sxs-lookup"><span data-stu-id="f1beb-138">Requirement</span></span> | <span data-ttu-id="f1beb-139">Значение</span><span class="sxs-lookup"><span data-stu-id="f1beb-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1beb-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1beb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f1beb-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1beb-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f1beb-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1beb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f1beb-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1beb-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f1beb-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1beb-144">Namespace</span></span><br/>                | <span data-ttu-id="f1beb-145">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="f1beb-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f1beb-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f1beb-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1beb-147"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1beb-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1beb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f1beb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1beb-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1beb-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1beb-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1beb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1beb-151">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="f1beb-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




