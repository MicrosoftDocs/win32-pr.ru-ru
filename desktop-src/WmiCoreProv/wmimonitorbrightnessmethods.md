---
description: Содержит методы, управляющие яркостью монитора.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Класс Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674018"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="b859a-103">Класс Вмимониторбригхтнессмесодс</span><span class="sxs-lookup"><span data-stu-id="b859a-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="b859a-104">Класс WMI **вмимониторбригхтнессмесодс** содержит методы, управляющие яркостью монитора.</span><span class="sxs-lookup"><span data-stu-id="b859a-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="b859a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b859a-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="b859a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b859a-106">Members</span></span>

<span data-ttu-id="b859a-107">Класс **вмимониторбригхтнессмесодс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b859a-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="b859a-108">Методы</span><span class="sxs-lookup"><span data-stu-id="b859a-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="b859a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b859a-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b859a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b859a-110">Methods</span></span>

<span data-ttu-id="b859a-111">Класс **вмимониторбригхтнессмесодс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b859a-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="b859a-112">Метод</span><span class="sxs-lookup"><span data-stu-id="b859a-112">Method</span></span>                                                                                                         | <span data-ttu-id="b859a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b859a-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="b859a-114">**вмиреверттополицибригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="b859a-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="b859a-115">Задает значение яркости для параметра политики.</span><span class="sxs-lookup"><span data-stu-id="b859a-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="b859a-116">**вмисеталсбригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="b859a-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="b859a-117">Задает значение яркости датчика окружающего освещения.</span><span class="sxs-lookup"><span data-stu-id="b859a-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="b859a-118">**вмисеталсбригхтнессстате**</span><span class="sxs-lookup"><span data-stu-id="b859a-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="b859a-119">Управляет состоянием яркости датчика внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="b859a-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="b859a-120">**вмисетбригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="b859a-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="b859a-121">Задает яркость монитора.</span><span class="sxs-lookup"><span data-stu-id="b859a-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="b859a-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="b859a-122">Properties</span></span>

<span data-ttu-id="b859a-123">Класс **вмимониторбригхтнессмесодс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b859a-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b859a-124">**Активен**</span><span class="sxs-lookup"><span data-stu-id="b859a-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b859a-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b859a-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b859a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b859a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b859a-127">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="b859a-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b859a-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b859a-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b859a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b859a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b859a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b859a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b859a-131">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="b859a-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b859a-132">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="b859a-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b859a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b859a-133">Requirements</span></span>



| <span data-ttu-id="b859a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b859a-134">Requirement</span></span> | <span data-ttu-id="b859a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b859a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b859a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b859a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b859a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b859a-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b859a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b859a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b859a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b859a-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b859a-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b859a-140">Namespace</span></span><br/>                | <span data-ttu-id="b859a-141">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="b859a-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b859a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b859a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b859a-143"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b859a-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b859a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b859a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b859a-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b859a-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b859a-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b859a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b859a-147">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="b859a-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




