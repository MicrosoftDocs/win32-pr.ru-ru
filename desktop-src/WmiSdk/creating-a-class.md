---
description: В инструментарии WMI класс — это объект, описывающий некоторые аспекты предприятия, например Специальный тип диска.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Создание класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674249"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="9bcb0-103">Создание класса WMI</span><span class="sxs-lookup"><span data-stu-id="9bcb0-103">Creating a WMI Class</span></span>

<span data-ttu-id="9bcb0-104">В инструментарии WMI класс — это объект, описывающий некоторые аспекты предприятия, например Специальный тип диска.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="9bcb0-105">После создания определения класса напишите библиотеку DLL поставщика для предоставления экземпляров класса, данных свойства и методов Execute, определенных для класса.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="9bcb0-106">Затем сценарии и приложения могут получать данные или управлять устройством.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="9bcb0-107">Дополнительные сведения см. [в разделе Разработка поставщика WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9bcb0-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="9bcb0-108">Чтобы гарантировать, что все определения классов WMI для управляемых объектов будут восстановлены в [*репозитории WMI*](gloss-w.md) , если в WMI произойдет сбой и перезапуститься, используйте инструкцию [**\# pragma автоматического восстановления**](pragma-autorecover.md) инструкции препроцессора в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="9bcb0-109">Базовый класс</span><span class="sxs-lookup"><span data-stu-id="9bcb0-109">Base Class</span></span>

<span data-ttu-id="9bcb0-110">Базовый класс представляет некоторую общую концепцию.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-110">A base class represents some general concept.</span></span> <span data-ttu-id="9bcb0-111">Например, класс [**CIM \_ кдромдриве**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) представляет все типы дисководов компакт-дисков в WMI и содержит общие свойства, описывающие все типы дисководов компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="9bcb0-112">Дополнительные сведения см. [в разделе Создание базового класса](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="9bcb0-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="9bcb0-113">Производный класс наследует свойства и методы от другого класса.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="9bcb0-114">Производный класс обычно представляет конкретный вариант базового класса.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="9bcb0-115">Например, класс [**Win32 \_ кдромдриве**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) представляет дисковод компакт-дисков в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="9bcb0-116">Класс **Win32 \_ кдромдриве** основан на и наследует многие свойства от [**CIM \_ кдромдриве**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="9bcb0-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="9bcb0-117">Однако **Win32 \_ кдромдриве**, как и другие производные классы, может иметь дополнительные свойства, которые делают производный класс уникальным.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="9bcb0-118">Дополнительные сведения см. [в разделе Создание производного класса](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="9bcb0-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="9bcb0-119">Свойства и методы</span><span class="sxs-lookup"><span data-stu-id="9bcb0-119">Properties and Methods</span></span>

<span data-ttu-id="9bcb0-120">Создание класса означает определение свойств, описывающих этот класс.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="9bcb0-121">Можно также определить методы, которые управляют объектом, представленным классом.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="9bcb0-122">Как правило, свойство представляет аспект объекта, например серийный номер устройства или размер в байтах для процесса, а метод представляет действие, которое изменяет состояние или поведение устройства или логической сущности.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="9bcb0-123">Каждый класс должен иметь по крайней мере одно ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-123">Each class must have at least one key property.</span></span> <span data-ttu-id="9bcb0-124">Хотя класс может иметь несколько ключей, нельзя создать экземпляр класса с более чем 256 ключами.</span><span class="sxs-lookup"><span data-stu-id="9bcb0-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bcb0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9bcb0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bcb0-126">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="9bcb0-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
