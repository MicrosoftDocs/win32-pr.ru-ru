---
description: Класс CIM \_ елементсеттинг представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Класс CIM_ElementSetting (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655919"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="47b91-103">Класс CIM_ElementSetting (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="47b91-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="47b91-104">Класс **CIM \_ елементсеттинг** представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.</span><span class="sxs-lookup"><span data-stu-id="47b91-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47b91-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="47b91-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="47b91-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="47b91-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="47b91-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="47b91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="47b91-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="47b91-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b91-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47b91-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="47b91-110">Члены</span><span class="sxs-lookup"><span data-stu-id="47b91-110">Members</span></span>

<span data-ttu-id="47b91-111">Класс **CIM \_ елементсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="47b91-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="47b91-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="47b91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47b91-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="47b91-113">Properties</span></span>

<span data-ttu-id="47b91-114">Класс **CIM \_ елементсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="47b91-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47b91-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="47b91-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b91-116">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="47b91-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="47b91-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b91-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b91-118">Ссылка на роль объекта [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) ассоциации **\_ елементсеттинг CIM** .</span><span class="sxs-lookup"><span data-stu-id="47b91-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="47b91-119">Связанный управляемый системный элемент предоставляет элемент, реализующий параметр элемента.</span><span class="sxs-lookup"><span data-stu-id="47b91-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="47b91-120">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="47b91-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b91-121">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="47b91-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="47b91-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b91-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b91-123">Ссылка на роль объекта [**\_ параметров CIM**](cim-setting.md) ассоциации **\_ елементсеттинг CIM** .</span><span class="sxs-lookup"><span data-stu-id="47b91-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="47b91-124">Связанный параметр предоставляет параметр, реализующий параметр элемента.</span><span class="sxs-lookup"><span data-stu-id="47b91-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47b91-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47b91-125">Remarks</span></span>

<span data-ttu-id="47b91-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="47b91-126">WMI does not implement this class.</span></span> <span data-ttu-id="47b91-127">Классы, производные от **CIM \_ елементсеттинг**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="47b91-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="47b91-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="47b91-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="47b91-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="47b91-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b91-130">Требования</span><span class="sxs-lookup"><span data-stu-id="47b91-130">Requirements</span></span>



| <span data-ttu-id="47b91-131">Требование</span><span class="sxs-lookup"><span data-stu-id="47b91-131">Requirement</span></span> | <span data-ttu-id="47b91-132">Значение</span><span class="sxs-lookup"><span data-stu-id="47b91-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47b91-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47b91-133">Minimum supported client</span></span><br/> | <span data-ttu-id="47b91-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47b91-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47b91-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47b91-135">Minimum supported server</span></span><br/> | <span data-ttu-id="47b91-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47b91-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47b91-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47b91-137">Namespace</span></span><br/>                | <span data-ttu-id="47b91-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="47b91-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47b91-139">MOF</span><span class="sxs-lookup"><span data-stu-id="47b91-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47b91-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47b91-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47b91-141">DLL</span><span class="sxs-lookup"><span data-stu-id="47b91-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47b91-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47b91-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




