---
description: '\_Класс WMI взаимосвязей Win32 логикалпрограмграупдиректори связывает логические группы программ (группирования в меню "Пуск") и каталоги файлов, в которых они хранятся.'
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Класс Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655671"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="d80f4-103">\_Класс Win32 логикалпрограмграупдиректори</span><span class="sxs-lookup"><span data-stu-id="d80f4-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="d80f4-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логикалпрограмграупдиректори** связывает логические группы программ (группирования в меню " **Пуск** ") и каталоги файлов, в которых они хранятся.</span><span class="sxs-lookup"><span data-stu-id="d80f4-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="d80f4-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d80f4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d80f4-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="d80f4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d80f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d80f4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d80f4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d80f4-108">Members</span></span>

<span data-ttu-id="d80f4-109">Класс **Win32 \_ логикалпрограмграупдиректори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d80f4-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="d80f4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d80f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d80f4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d80f4-111">Properties</span></span>

<span data-ttu-id="d80f4-112">Класс **Win32 \_ логикалпрограмграупдиректори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d80f4-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d80f4-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d80f4-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d80f4-114">Тип данных: **Win32 \_ логикалпрограмграуп**</span><span class="sxs-lookup"><span data-stu-id="d80f4-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="d80f4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d80f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d80f4-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ логикалпрограмграуп")</span><span class="sxs-lookup"><span data-stu-id="d80f4-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="d80f4-117">Ссылка на экземпляр, представляющий логическую группу программ.</span><span class="sxs-lookup"><span data-stu-id="d80f4-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="d80f4-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="d80f4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d80f4-119">Тип данных: **\_ Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="d80f4-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="d80f4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d80f4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d80f4-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI- \| \_ Каталог Win32")</span><span class="sxs-lookup"><span data-stu-id="d80f4-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="d80f4-122">Ссылка на экземпляр, представляющий каталог файлов для логической группы программ.</span><span class="sxs-lookup"><span data-stu-id="d80f4-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d80f4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d80f4-123">Remarks</span></span>

<span data-ttu-id="d80f4-124">Класс **Win32 \_ логикалпрограмграупдиректори** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d80f4-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d80f4-125">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="d80f4-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="d80f4-126">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="d80f4-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="d80f4-127">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d80f4-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="d80f4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d80f4-128">Requirements</span></span>



| <span data-ttu-id="d80f4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d80f4-129">Requirement</span></span> | <span data-ttu-id="d80f4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d80f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d80f4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d80f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d80f4-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d80f4-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d80f4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d80f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d80f4-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d80f4-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d80f4-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d80f4-135">Namespace</span></span><br/>                | <span data-ttu-id="d80f4-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d80f4-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d80f4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d80f4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d80f4-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d80f4-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d80f4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d80f4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d80f4-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d80f4-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80f4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d80f4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80f4-142">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="d80f4-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="d80f4-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d80f4-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

