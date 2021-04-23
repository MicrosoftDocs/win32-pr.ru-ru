---
description: WMI определяет набор системных свойств, которые связаны со всеми классами и экземплярами классов в дополнение к свойствам, зависящим от класса.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Свойства системы CIM для объектов MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712112"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="af12f-103">Свойства системы CIM для объектов MIB</span><span class="sxs-lookup"><span data-stu-id="af12f-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="af12f-104">WMI определяет набор системных свойств, которые связаны со всеми классами и экземплярами классов в дополнение к свойствам, зависящим от класса.</span><span class="sxs-lookup"><span data-stu-id="af12f-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="af12f-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="af12f-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="af12f-106">Поставщик SNMP использует следующие свойства системы CIM при сопоставлении определений объектов MIB с определениями классов CIM.</span><span class="sxs-lookup"><span data-stu-id="af12f-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="af12f-107">Чтобы поставщик SNMP полностью разрешил объект группы, должны присутствовать обязательные свойства.</span><span class="sxs-lookup"><span data-stu-id="af12f-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="af12f-108">Сбой определения обязательного свойства возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="af12f-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="af12f-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="af12f-109">Property</span></span></th>
<th><span data-ttu-id="af12f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="af12f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af12f-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="af12f-112"><strong>строка</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-113">Для экземпляров — класс, которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="af12f-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="af12f-114">Для классов это имя класса.</span><span class="sxs-lookup"><span data-stu-id="af12f-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af12f-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="af12f-116"><strong>строка</strong> Используемых</span><span class="sxs-lookup"><span data-stu-id="af12f-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="af12f-117">Имя класса, который является конечным базовым классом для текущего объекта (не его непосредственным родительским классом).</span><span class="sxs-lookup"><span data-stu-id="af12f-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af12f-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="af12f-119"><strong>UInt32</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-120">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="af12f-120">Type of object.</span></span> <span data-ttu-id="af12f-121">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="af12f-121">Values are:</span></span><br/> <dl> <span data-ttu-id="af12f-122">1 = класс</span><span class="sxs-lookup"><span data-stu-id="af12f-122">1 = class</span></span><br />
<span data-ttu-id="af12f-123">2 = экземпляр</span><span class="sxs-lookup"><span data-stu-id="af12f-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af12f-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="af12f-125"><strong>строка</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-126">Пространство имен, в котором находится объект.</span><span class="sxs-lookup"><span data-stu-id="af12f-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af12f-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="af12f-128"><strong>строка</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-129">Абсолютный путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="af12f-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af12f-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="af12f-131"><strong>UInt32</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-132">Количество несистемных свойств, определенных для объекта.</span><span class="sxs-lookup"><span data-stu-id="af12f-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af12f-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="af12f-134"><strong>строка</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-135">Относительный путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="af12f-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af12f-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="af12f-137"><strong>строка</strong> Заполнен</span><span class="sxs-lookup"><span data-stu-id="af12f-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="af12f-138">Сервер, предоставляющий объект.</span><span class="sxs-lookup"><span data-stu-id="af12f-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af12f-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="af12f-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="af12f-140"><strong>строка</strong> Используемых</span><span class="sxs-lookup"><span data-stu-id="af12f-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="af12f-141">Непосредственный родительский класс объекта.</span><span class="sxs-lookup"><span data-stu-id="af12f-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




