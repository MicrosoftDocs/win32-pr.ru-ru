---
description: '\_Класс WMI взаимосвязей Win32 оператингсистемкфе связывает операционную систему и обновления продукта, примененные как представленные в Win32 \_ куиккфиксенгиниринг.'
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Класс Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990729"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="3c78e-103">\_Класс Win32 оператингсистемкфе</span><span class="sxs-lookup"><span data-stu-id="3c78e-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="3c78e-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ оператингсистемкфе** связывает операционную систему и обновления продукта, примененные как представленные в [**Win32 \_ куиккфиксенгиниринг**](win32-quickfixengineering.md).</span><span class="sxs-lookup"><span data-stu-id="3c78e-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="3c78e-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3c78e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3c78e-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="3c78e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c78e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c78e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3c78e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3c78e-108">Members</span></span>

<span data-ttu-id="3c78e-109">Класс **Win32 \_ оператингсистемкфе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c78e-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="3c78e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c78e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c78e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c78e-111">Properties</span></span>

<span data-ttu-id="3c78e-112">Класс **Win32 \_ оператингсистемкфе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c78e-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c78e-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="3c78e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c78e-114">Тип данных: **Win32 с \_ операционной** системы</span><span class="sxs-lookup"><span data-stu-id="3c78e-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3c78e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c78e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c78e-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="3c78e-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3c78e-117">Ссылка на экземпляр, представляющий систему, затронутую обновлением продукта в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="3c78e-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3c78e-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="3c78e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c78e-119">Тип данных: **Win32 \_ куиккфиксенгиниринг**</span><span class="sxs-lookup"><span data-stu-id="3c78e-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="3c78e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c78e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c78e-121">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**слабый**](../wmisdk/standard-qualifiers.md), [**переопределяющий**](../wmisdk/standard-qualifiers.md) ("зависимый"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ куиккфиксенгиниринг")</span><span class="sxs-lookup"><span data-stu-id="3c78e-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="3c78e-122">Ссылка на экземпляр, представляющий экземпляр объекта, применяемого к операционной системе в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="3c78e-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c78e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c78e-123">Remarks</span></span>

<span data-ttu-id="3c78e-124">Класс **Win32 \_ оператингсистемкфе** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3c78e-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c78e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3c78e-125">Requirements</span></span>



| <span data-ttu-id="3c78e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3c78e-126">Requirement</span></span> | <span data-ttu-id="3c78e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3c78e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c78e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c78e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c78e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c78e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c78e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c78e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c78e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c78e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c78e-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c78e-132">Namespace</span></span><br/>                | <span data-ttu-id="3c78e-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3c78e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c78e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3c78e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c78e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c78e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c78e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3c78e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c78e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c78e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c78e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c78e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c78e-139">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="3c78e-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="3c78e-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="3c78e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
