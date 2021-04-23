---
description: '\_Класс WMI взаимосвязей Win32 програмграупконтентс связывает порядок групп программ и отдельную группу программ или элемент, содержащийся в нем.'
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Класс Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072378"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="daec0-103">\_Класс Win32 програмграупконтентс</span><span class="sxs-lookup"><span data-stu-id="daec0-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="daec0-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ програмграупконтентс** связывает порядок групп программ и отдельную группу программ или элемент, содержащийся в нем.</span><span class="sxs-lookup"><span data-stu-id="daec0-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="daec0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="daec0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="daec0-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="daec0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="daec0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daec0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="daec0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="daec0-108">Members</span></span>

<span data-ttu-id="daec0-109">Класс **Win32 \_ програмграупконтентс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="daec0-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="daec0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="daec0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="daec0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="daec0-111">Properties</span></span>

<span data-ttu-id="daec0-112">Класс **Win32 \_ програмграупконтентс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="daec0-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="daec0-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="daec0-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daec0-114">Тип данных: **Win32 \_ логикалпрограмграуп**</span><span class="sxs-lookup"><span data-stu-id="daec0-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="daec0-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="daec0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="daec0-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ логикалпрограмграуп")</span><span class="sxs-lookup"><span data-stu-id="daec0-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="daec0-117">Ссылка на экземпляр, представляющий логическую группу программ для этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="daec0-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="daec0-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="daec0-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daec0-119">Тип данных: **Win32 \_ програмграупоритем**</span><span class="sxs-lookup"><span data-stu-id="daec0-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="daec0-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="daec0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="daec0-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ програмграупоритем")</span><span class="sxs-lookup"><span data-stu-id="daec0-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="daec0-122">Ссылка на экземпляр, представляющий группу меню " **Пуск** " или элемент для этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="daec0-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daec0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="daec0-123">Remarks</span></span>

<span data-ttu-id="daec0-124">Класс **Win32 \_ програмграупконтентс** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="daec0-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="daec0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="daec0-125">Requirements</span></span>



| <span data-ttu-id="daec0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="daec0-126">Requirement</span></span> | <span data-ttu-id="daec0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="daec0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="daec0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daec0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="daec0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="daec0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="daec0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daec0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="daec0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daec0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="daec0-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="daec0-132">Namespace</span></span><br/>                | <span data-ttu-id="daec0-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="daec0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="daec0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="daec0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="daec0-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="daec0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="daec0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="daec0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daec0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daec0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daec0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daec0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daec0-139">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="daec0-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="daec0-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="daec0-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
