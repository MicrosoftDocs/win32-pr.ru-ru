---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM коллектедмсес представляет члены объекта GROUPING, класса коллектионофмсес.'
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: Класс CIM_CollectedMSEs (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496410"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="4eb9d-103">Класс CIM_CollectedMSEs (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4eb9d-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4eb9d-104">Класс сопоставления **CIM \_ коллектедмсес** представляет члены объекта GROUPING, класса [**коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb9d-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eb9d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4eb9d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4eb9d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4eb9d-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4eb9d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb9d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eb9d-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="4eb9d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4eb9d-110">Members</span></span>

<span data-ttu-id="4eb9d-111">Класс **CIM \_ коллектедмсес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4eb9d-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="4eb9d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4eb9d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4eb9d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4eb9d-113">Properties</span></span>

<span data-ttu-id="4eb9d-114">Класс **CIM \_ коллектедмсес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4eb9d-115">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb9d-116">Тип данных: **cm \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="4eb9d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eb9d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eb9d-118">Ссылка на объект группирования или контейнера, представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="4eb9d-119">**Член**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb9d-120">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4eb9d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eb9d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eb9d-122">Ссылка на элемент коллекции.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eb9d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eb9d-123">Remarks</span></span>

<span data-ttu-id="4eb9d-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-124">WMI does not implement this class.</span></span> <span data-ttu-id="4eb9d-125">Дополнительные сведения о классах WMI, производных от **CIM \_ коллектедмсес**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4eb9d-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4eb9d-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4eb9d-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4eb9d-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb9d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb9d-128">Requirements</span></span>



| <span data-ttu-id="4eb9d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb9d-129">Requirement</span></span> | <span data-ttu-id="4eb9d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb9d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb9d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb9d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb9d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4eb9d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4eb9d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb9d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb9d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4eb9d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4eb9d-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4eb9d-135">Namespace</span></span><br/>                | <span data-ttu-id="4eb9d-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4eb9d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4eb9d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4eb9d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4eb9d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4eb9d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4eb9d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4eb9d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eb9d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eb9d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




