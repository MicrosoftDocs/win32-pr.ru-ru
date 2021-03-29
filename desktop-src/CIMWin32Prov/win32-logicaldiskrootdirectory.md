---
description: '\_Класс WMI взаимосвязей Win32 логикалдискрутдиректори связывает логический диск и структуру каталогов.'
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Класс Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895393"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="7921a-103">\_Класс Win32 логикалдискрутдиректори</span><span class="sxs-lookup"><span data-stu-id="7921a-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="7921a-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логикалдискрутдиректори** связывает логический диск и структуру каталогов.</span><span class="sxs-lookup"><span data-stu-id="7921a-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="7921a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7921a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7921a-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="7921a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7921a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7921a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7921a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7921a-108">Members</span></span>

<span data-ttu-id="7921a-109">Класс **Win32 \_ логикалдискрутдиректори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7921a-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="7921a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7921a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7921a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7921a-111">Properties</span></span>

<span data-ttu-id="7921a-112">Класс **Win32 \_ логикалдискрутдиректори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7921a-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7921a-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="7921a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7921a-114">Тип данных: **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="7921a-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="7921a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7921a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7921a-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="7921a-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="7921a-117">Ссылка на экземпляр, представляющий свойства логического диска.</span><span class="sxs-lookup"><span data-stu-id="7921a-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="7921a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7921a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7921a-119">Тип данных: **\_ Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="7921a-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="7921a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7921a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7921a-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI- \| \_ Каталог Win32")</span><span class="sxs-lookup"><span data-stu-id="7921a-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="7921a-122">Ссылка на экземпляр, представляющий свойства структуры каталогов файлов.</span><span class="sxs-lookup"><span data-stu-id="7921a-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7921a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7921a-123">Remarks</span></span>

<span data-ttu-id="7921a-124">Класс **Win32 \_ логикалдискрутдиректори** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="7921a-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7921a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7921a-125">Requirements</span></span>



| <span data-ttu-id="7921a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7921a-126">Requirement</span></span> | <span data-ttu-id="7921a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7921a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7921a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7921a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7921a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7921a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7921a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7921a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7921a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7921a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7921a-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7921a-132">Namespace</span></span><br/>                | <span data-ttu-id="7921a-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7921a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7921a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7921a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7921a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7921a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7921a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7921a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7921a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7921a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7921a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7921a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7921a-139">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="7921a-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="7921a-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7921a-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

