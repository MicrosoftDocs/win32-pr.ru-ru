---
description: Содержит методы, получающие необработанное содержимое определения входных данных видео с расширенными расширенными данными идентификации (E-EDID) v. 1. x стандартных блоков данных 128-Byte.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Класс Вмимонитордескриптормесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674104"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="da58c-103">Класс Вмимонитордескриптормесодс</span><span class="sxs-lookup"><span data-stu-id="da58c-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="da58c-104">Класс WMI **вмимонитордескриптормесодс** содержит методы, которые получают необработанное содержимое распознавания видео с расширенными расширенными данными идентификации (E-EDID) v. 1. x стандартных блоков данных 128-Byte.</span><span class="sxs-lookup"><span data-stu-id="da58c-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="da58c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da58c-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="da58c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="da58c-106">Members</span></span>

<span data-ttu-id="da58c-107">Класс **вмимонитордескриптормесодс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="da58c-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="da58c-108">Методы</span><span class="sxs-lookup"><span data-stu-id="da58c-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="da58c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="da58c-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da58c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="da58c-110">Methods</span></span>

<span data-ttu-id="da58c-111">Класс **вмимонитордескриптормесодс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="da58c-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="da58c-112">Метод</span><span class="sxs-lookup"><span data-stu-id="da58c-112">Method</span></span>                                                                                           | <span data-ttu-id="da58c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="da58c-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="da58c-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="da58c-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="da58c-115">Обращается к необработанным данным для указанного блока дескрипторов EDID v. 1. x.</span><span class="sxs-lookup"><span data-stu-id="da58c-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da58c-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="da58c-116">Properties</span></span>

<span data-ttu-id="da58c-117">Класс **вмимонитордескриптормесодс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="da58c-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da58c-118">**Активен**</span><span class="sxs-lookup"><span data-stu-id="da58c-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da58c-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="da58c-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da58c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="da58c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da58c-121">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="da58c-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="da58c-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="da58c-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da58c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="da58c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da58c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="da58c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da58c-125">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="da58c-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da58c-126">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="da58c-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da58c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="da58c-127">Requirements</span></span>



| <span data-ttu-id="da58c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="da58c-128">Requirement</span></span> | <span data-ttu-id="da58c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="da58c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da58c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da58c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="da58c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da58c-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da58c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da58c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="da58c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da58c-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da58c-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="da58c-134">Namespace</span></span><br/>                | <span data-ttu-id="da58c-135">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="da58c-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="da58c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="da58c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da58c-137"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da58c-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="da58c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="da58c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da58c-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da58c-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da58c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da58c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da58c-141">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="da58c-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




