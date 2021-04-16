---
description: Представляет изменение яркости монитора.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Класс Вмимониторбригхтнессевент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702725"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="b27f3-103">Класс Вмимониторбригхтнессевент</span><span class="sxs-lookup"><span data-stu-id="b27f3-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="b27f3-104">Класс событий WMI **вмимониторбригхтнессевент** представляет изменение яркости монитора.</span><span class="sxs-lookup"><span data-stu-id="b27f3-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b27f3-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="b27f3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b27f3-106">Members</span></span>

<span data-ttu-id="b27f3-107">Класс **вмимониторбригхтнессевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b27f3-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b27f3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="b27f3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b27f3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b27f3-109">Properties</span></span>

<span data-ttu-id="b27f3-110">Класс **вмимониторбригхтнессевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b27f3-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b27f3-111">**Активен**</span><span class="sxs-lookup"><span data-stu-id="b27f3-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b27f3-112">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b27f3-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b27f3-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b27f3-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b27f3-114">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="b27f3-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b27f3-115">**Brightness**</span><span class="sxs-lookup"><span data-stu-id="b27f3-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b27f3-116">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b27f3-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b27f3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b27f3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b27f3-118">Текущая яркость монитора в процентах.</span><span class="sxs-lookup"><span data-stu-id="b27f3-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="b27f3-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b27f3-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b27f3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b27f3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b27f3-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b27f3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b27f3-122">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="b27f3-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b27f3-123">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="b27f3-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b27f3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b27f3-124">Requirements</span></span>



| <span data-ttu-id="b27f3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b27f3-125">Requirement</span></span> | <span data-ttu-id="b27f3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b27f3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b27f3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b27f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b27f3-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b27f3-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b27f3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b27f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b27f3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b27f3-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b27f3-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b27f3-131">Namespace</span></span><br/>                | <span data-ttu-id="b27f3-132">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="b27f3-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b27f3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b27f3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b27f3-134"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b27f3-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b27f3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b27f3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b27f3-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b27f3-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27f3-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b27f3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27f3-138">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="b27f3-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="b27f3-139">**вмимониторбригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="b27f3-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="b27f3-140">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="b27f3-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

