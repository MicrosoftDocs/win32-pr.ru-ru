---
description: Класс CIM \_ логикалидентити — это абстрактная и универсальная ассоциация, которая указывает, что два логических элемента представляют различные аспекты одной и той же базовой сущности.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: Класс CIM_LogicalIdentity (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990434"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="84228-103">Класс CIM_LogicalIdentity (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="84228-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="84228-104">Класс **CIM \_ логикалидентити** — это абстрактная и универсальная ассоциация, которая указывает, что два логических элемента представляют различные аспекты одной и той же базовой сущности.</span><span class="sxs-lookup"><span data-stu-id="84228-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="84228-105">Ассоциация передает то, что можно определить с помощью множественного наследования и ограничено логическими аспектами управляемого элемента System.</span><span class="sxs-lookup"><span data-stu-id="84228-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="84228-106">В большинстве случаев отношение удостоверений определяется эквивалентностью ключей или другими идентифицирующими свойствами связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="84228-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="84228-107">Ассоциация должна использоваться только в тех сценариях, которые хорошо понятны, что позволяет более конкретное определение и уточнение в подклассах.</span><span class="sxs-lookup"><span data-stu-id="84228-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="84228-108">Сценарий, в котором целесообразно отношение, например, представляет устройство, которое является как сущностью шины, так и функциональной сущностью, где устройство — это объект USB (шина) и клавиатура (функциональный).</span><span class="sxs-lookup"><span data-stu-id="84228-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84228-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="84228-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84228-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84228-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84228-111">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="84228-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="84228-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="84228-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84228-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84228-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="84228-114">Члены</span><span class="sxs-lookup"><span data-stu-id="84228-114">Members</span></span>

<span data-ttu-id="84228-115">Класс **CIM \_ логикалидентити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84228-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="84228-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="84228-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84228-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="84228-117">Properties</span></span>

<span data-ttu-id="84228-118">Класс **CIM \_ логикалидентити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84228-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84228-119">**самилемент**</span><span class="sxs-lookup"><span data-stu-id="84228-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84228-120">Тип данных: **CIM \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="84228-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="84228-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84228-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84228-122">Ссылка на альтернативный аспект системной сущности.</span><span class="sxs-lookup"><span data-stu-id="84228-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="84228-123">**системелемент**</span><span class="sxs-lookup"><span data-stu-id="84228-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84228-124">Тип данных: **CIM \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="84228-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="84228-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84228-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84228-126">Ссылка на один аспект логического элемента.</span><span class="sxs-lookup"><span data-stu-id="84228-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84228-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84228-127">Remarks</span></span>

<span data-ttu-id="84228-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="84228-128">WMI does not implement this class.</span></span> <span data-ttu-id="84228-129">Классы, производные от **CIM \_ логикалидентити**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="84228-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="84228-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="84228-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84228-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="84228-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84228-132">Требования</span><span class="sxs-lookup"><span data-stu-id="84228-132">Requirements</span></span>



| <span data-ttu-id="84228-133">Требование</span><span class="sxs-lookup"><span data-stu-id="84228-133">Requirement</span></span> | <span data-ttu-id="84228-134">Значение</span><span class="sxs-lookup"><span data-stu-id="84228-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84228-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84228-135">Minimum supported client</span></span><br/> | <span data-ttu-id="84228-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84228-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84228-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84228-137">Minimum supported server</span></span><br/> | <span data-ttu-id="84228-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84228-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84228-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84228-139">Namespace</span></span><br/>                | <span data-ttu-id="84228-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84228-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84228-141">MOF</span><span class="sxs-lookup"><span data-stu-id="84228-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84228-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84228-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84228-143">DLL</span><span class="sxs-lookup"><span data-stu-id="84228-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84228-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84228-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




