---
description: Класс CIM \_ бутосфромфс связывает операционную систему и файловые системы, из которых загружается операционная система.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: Класс CIM_BootOSFromFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990645"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="0b3ef-103">\_Класс CIM бутосфромфс</span><span class="sxs-lookup"><span data-stu-id="0b3ef-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="0b3ef-104">Класс **CIM \_ бутосфромфс** связывает операционную систему и файловые системы, из которых загружается операционная система.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="0b3ef-105">Ассоциация — «многие ко многим»; Распределенная операционная система может зависеть от нескольких файловых систем для правильной и полной загрузки.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b3ef-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b3ef-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b3ef-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b3ef-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b3ef-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3ef-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b3ef-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0b3ef-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0b3ef-111">Members</span></span>

<span data-ttu-id="0b3ef-112">Класс **CIM \_ бутосфромфс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0b3ef-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="0b3ef-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b3ef-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b3ef-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b3ef-114">Properties</span></span>

<span data-ttu-id="0b3ef-115">Класс **CIM \_ бутосфромфс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b3ef-116">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0b3ef-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b3ef-117">Тип данных: **\_ Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="0b3ef-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0b3ef-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b3ef-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b3ef-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0b3ef-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0b3ef-120">Файловая система, из которой загружается операционная система.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0b3ef-121">**Него**</span><span class="sxs-lookup"><span data-stu-id="0b3ef-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b3ef-122">Тип данных: **\_ Операционная система CIM**</span><span class="sxs-lookup"><span data-stu-id="0b3ef-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0b3ef-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b3ef-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b3ef-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0b3ef-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0b3ef-125">Операционная система.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b3ef-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b3ef-126">Remarks</span></span>

<span data-ttu-id="0b3ef-127">Класс **CIM \_ бутосфромфс** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0b3ef-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0b3ef-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-128">WMI does not implement this class.</span></span>

<span data-ttu-id="0b3ef-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b3ef-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b3ef-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0b3ef-131">Requirements</span></span>



| <span data-ttu-id="0b3ef-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0b3ef-132">Requirement</span></span> | <span data-ttu-id="0b3ef-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0b3ef-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3ef-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b3ef-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3ef-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b3ef-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b3ef-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b3ef-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3ef-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b3ef-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b3ef-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0b3ef-138">Namespace</span></span><br/>                | <span data-ttu-id="0b3ef-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0b3ef-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b3ef-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0b3ef-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b3ef-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b3ef-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b3ef-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0b3ef-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b3ef-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b3ef-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3ef-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b3ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3ef-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="0b3ef-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

