---
description: Класс CIM \_ коллектионсеттинг представляет ассоциацию между CIM- \_ коллектионофмсес и классом параметра, определенным для них.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Класс CIM_CollectionSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896109"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="bc5d0-103">\_Класс CIM коллектионсеттинг</span><span class="sxs-lookup"><span data-stu-id="bc5d0-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="bc5d0-104">Класс **CIM \_ коллектионсеттинг** представляет ассоциацию между CIM- [**\_ коллектионофмсес**](cim-collectionofmses.md) и классом параметра, определенным для них.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc5d0-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bc5d0-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bc5d0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bc5d0-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bc5d0-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5d0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc5d0-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="bc5d0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="bc5d0-110">Members</span></span>

<span data-ttu-id="bc5d0-111">Класс **CIM \_ коллектионсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bc5d0-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bc5d0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc5d0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc5d0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc5d0-113">Properties</span></span>

<span data-ttu-id="bc5d0-114">Класс **CIM \_ коллектионсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc5d0-115">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc5d0-116">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="bc5d0-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc5d0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc5d0-118">Ссылка на класс [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="bc5d0-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="bc5d0-119">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc5d0-120">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="bc5d0-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc5d0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc5d0-122">Ссылка на объект **Setting** , связанный со свойством **Collection** .</span><span class="sxs-lookup"><span data-stu-id="bc5d0-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc5d0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc5d0-123">Remarks</span></span>

<span data-ttu-id="bc5d0-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-124">WMI does not implement this class.</span></span> <span data-ttu-id="bc5d0-125">Дополнительные сведения о классах WMI, производных от **CIM \_ коллектионсеттинг**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bc5d0-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bc5d0-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bc5d0-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="bc5d0-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc5d0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bc5d0-128">Requirements</span></span>



| <span data-ttu-id="bc5d0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bc5d0-129">Requirement</span></span> | <span data-ttu-id="bc5d0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bc5d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5d0-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc5d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bc5d0-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc5d0-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc5d0-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc5d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bc5d0-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc5d0-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc5d0-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bc5d0-135">Namespace</span></span><br/>                | <span data-ttu-id="bc5d0-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc5d0-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bc5d0-137">MOF</span><span class="sxs-lookup"><span data-stu-id="bc5d0-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc5d0-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc5d0-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc5d0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bc5d0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc5d0-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc5d0-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




