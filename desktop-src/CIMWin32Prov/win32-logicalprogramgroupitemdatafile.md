---
description: '\_Класс WMI взаимосвязей Win32 логикалпрограмграупитемдатафиле связывает элементы группы программ меню Пуск и файлы, в которых они хранятся.'
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Класс Win32_LogicalProgramGroupItemDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142853"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="f1fa9-103">\_Класс Win32 логикалпрограмграупитемдатафиле</span><span class="sxs-lookup"><span data-stu-id="f1fa9-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="f1fa9-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логикалпрограмграупитемдатафиле** связывает элементы группы программ меню **Пуск** и файлы, в которых они хранятся.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="f1fa9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f1fa9-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fa9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1fa9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f1fa9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f1fa9-108">Members</span></span>

<span data-ttu-id="f1fa9-109">Класс **Win32 \_ логикалпрограмграупитемдатафиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f1fa9-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="f1fa9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1fa9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1fa9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1fa9-111">Properties</span></span>

<span data-ttu-id="f1fa9-112">Класс **Win32 \_ логикалпрограмграупитемдатафиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1fa9-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f1fa9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fa9-114">Тип данных: **Win32 \_ логикалпрограмграупитем**</span><span class="sxs-lookup"><span data-stu-id="f1fa9-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="f1fa9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1fa9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fa9-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ логикалпрограмграупитем")</span><span class="sxs-lookup"><span data-stu-id="f1fa9-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="f1fa9-117">Ссылка на экземпляр, представляющий группы программ в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="f1fa9-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="f1fa9-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="f1fa9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fa9-119">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="f1fa9-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="f1fa9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1fa9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fa9-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ File")</span><span class="sxs-lookup"><span data-stu-id="f1fa9-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="f1fa9-122">Ссылка на экземпляр, представляющий класс, связанный с группой программ.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1fa9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1fa9-123">Remarks</span></span>

<span data-ttu-id="f1fa9-124">Класс **Win32 \_ логикалпрограмграупитемдатафиле** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f1fa9-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f1fa9-125">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="f1fa9-126">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="f1fa9-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="f1fa9-127">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="f1fa9-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1fa9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f1fa9-128">Requirements</span></span>



| <span data-ttu-id="f1fa9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f1fa9-129">Requirement</span></span> | <span data-ttu-id="f1fa9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f1fa9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fa9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1fa9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fa9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1fa9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1fa9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1fa9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fa9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1fa9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1fa9-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1fa9-135">Namespace</span></span><br/>                | <span data-ttu-id="f1fa9-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1fa9-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1fa9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f1fa9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1fa9-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1fa9-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1fa9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fa9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fa9-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fa9-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1fa9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1fa9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fa9-142">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f1fa9-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="f1fa9-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1fa9-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

