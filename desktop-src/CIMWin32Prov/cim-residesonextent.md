---
description: Класс CIM \_ ресидесонекстент представляет ассоциацию между файловой системой и областью хранения, в которой она находится. Как правило, файловая система находится на логическом диске.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: Класс CIM_ResidesOnExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142754"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="5d6c8-104">\_Класс CIM ресидесонекстент</span><span class="sxs-lookup"><span data-stu-id="5d6c8-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="5d6c8-105">Класс **CIM \_ ресидесонекстент** представляет ассоциацию между файловой системой и областью хранения, в которой она находится.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="5d6c8-106">Как правило, файловая система находится на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d6c8-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d6c8-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d6c8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d6c8-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5d6c8-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6c8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d6c8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5d6c8-112">Члены</span><span class="sxs-lookup"><span data-stu-id="5d6c8-112">Members</span></span>

<span data-ttu-id="5d6c8-113">Класс **CIM \_ ресидесонекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d6c8-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="5d6c8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d6c8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d6c8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d6c8-115">Properties</span></span>

<span data-ttu-id="5d6c8-116">Класс **CIM \_ ресидесонекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d6c8-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="5d6c8-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6c8-118">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="5d6c8-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="5d6c8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6c8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6c8-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="5d6c8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5d6c8-121">[**\_ Сторажеекстент CIM**](cim-storageextent.md) , описывающий экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="5d6c8-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="5d6c8-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6c8-123">Тип данных: **\_ Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="5d6c8-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5d6c8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6c8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6c8-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="5d6c8-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5d6c8-126">Файловая система [**CIM \_**](cim-filesystem.md) с описанием файловой системы, расположенной в экстенте хранения.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d6c8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d6c8-127">Remarks</span></span>

<span data-ttu-id="5d6c8-128">Класс **CIM \_ ресидесонекстент** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5d6c8-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5d6c8-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-129">WMI does not implement this class.</span></span>

<span data-ttu-id="5d6c8-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d6c8-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5d6c8-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6c8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5d6c8-132">Requirements</span></span>



| <span data-ttu-id="5d6c8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5d6c8-133">Requirement</span></span> | <span data-ttu-id="5d6c8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5d6c8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6c8-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d6c8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6c8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d6c8-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d6c8-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d6c8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6c8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d6c8-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d6c8-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5d6c8-139">Namespace</span></span><br/>                | <span data-ttu-id="5d6c8-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d6c8-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d6c8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5d6c8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d6c8-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d6c8-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d6c8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6c8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6c8-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d6c8-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d6c8-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d6c8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6c8-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="5d6c8-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

