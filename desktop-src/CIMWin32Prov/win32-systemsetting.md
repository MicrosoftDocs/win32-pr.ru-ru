---
description: '\_Класс WMI абстрактных ассоциаций Win32 системсеттинг связывает компьютерную систему и общий параметр в этой системе.'
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Класс Win32_SystemSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496674"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="a86c8-103">\_Класс Win32 системсеттинг</span><span class="sxs-lookup"><span data-stu-id="a86c8-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="a86c8-104">[Класс WMI](../wmisdk/retrieving-a-class.md) абстрактных ассоциаций **Win32 \_ системсеттинг** связывает компьютерную систему и общий параметр в этой системе.</span><span class="sxs-lookup"><span data-stu-id="a86c8-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="a86c8-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a86c8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a86c8-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="a86c8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a86c8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a86c8-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="a86c8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a86c8-108">Members</span></span>

<span data-ttu-id="a86c8-109">Класс **Win32 \_ системсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a86c8-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="a86c8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a86c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a86c8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a86c8-111">Properties</span></span>

<span data-ttu-id="a86c8-112">Класс **Win32 \_ системсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a86c8-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a86c8-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a86c8-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a86c8-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a86c8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a86c8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a86c8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a86c8-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="a86c8-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a86c8-117">Ссылка на экземпляр, представляющий свойства компьютерной системы, в которой можно применить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a86c8-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="a86c8-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="a86c8-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a86c8-119">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="a86c8-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="a86c8-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a86c8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a86c8-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| параметр CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="a86c8-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="a86c8-122">Ссылка на экземпляр, представляющий свойства параметра, который может быть применен к компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="a86c8-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a86c8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a86c8-123">Remarks</span></span>

<span data-ttu-id="a86c8-124">Класс **Win32 \_ системсеттинг** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="a86c8-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a86c8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a86c8-125">Requirements</span></span>



| <span data-ttu-id="a86c8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a86c8-126">Requirement</span></span> | <span data-ttu-id="a86c8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a86c8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a86c8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a86c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a86c8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a86c8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a86c8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a86c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a86c8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a86c8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a86c8-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a86c8-132">Namespace</span></span><br/>                | <span data-ttu-id="a86c8-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a86c8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a86c8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a86c8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a86c8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a86c8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a86c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a86c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a86c8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a86c8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86c8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a86c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86c8-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="a86c8-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="a86c8-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="a86c8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
