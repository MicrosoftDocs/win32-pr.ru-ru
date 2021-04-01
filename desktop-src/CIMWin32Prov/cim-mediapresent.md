---
description: '\_Ассоциация МЕДИАПРЕСЕНТ CIM описывает связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.'
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: Класс CIM_MediaPresent (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914159"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="7ad09-103">Класс CIM_MediaPresent (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7ad09-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7ad09-104">Ассоциация **\_ медиапресент CIM** описывает связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="7ad09-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ad09-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7ad09-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7ad09-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7ad09-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7ad09-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7ad09-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7ad09-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7ad09-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad09-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ad09-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7ad09-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7ad09-110">Members</span></span>

<span data-ttu-id="7ad09-111">Класс **CIM \_ медиапресент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ad09-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="7ad09-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ad09-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ad09-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ad09-113">Properties</span></span>

<span data-ttu-id="7ad09-114">Класс **CIM \_ медиапресент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7ad09-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ad09-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7ad09-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad09-116">Тип данных: **CIM \_ медиаакцессдевице**</span><span class="sxs-lookup"><span data-stu-id="7ad09-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7ad09-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ad09-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ad09-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7ad09-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7ad09-119">[**\_ Медиаакцессдевице CIM**](cim-mediaaccessdevice.md) , описывающий устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="7ad09-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="7ad09-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="7ad09-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad09-121">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="7ad09-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="7ad09-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ad09-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ad09-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="7ad09-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7ad09-124">[**\_ Сторажеекстент CIM**](cim-storageextent.md) , описывающий экстент хранения, к которому осуществляется доступ с помощью устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="7ad09-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ad09-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ad09-125">Remarks</span></span>

<span data-ttu-id="7ad09-126">Класс **CIM \_ медиапресент** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7ad09-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7ad09-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7ad09-127">WMI does not implement this class.</span></span> <span data-ttu-id="7ad09-128">Классы, производные от **CIM \_ медиапресент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7ad09-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7ad09-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7ad09-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7ad09-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7ad09-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad09-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7ad09-131">Requirements</span></span>



| <span data-ttu-id="7ad09-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7ad09-132">Requirement</span></span> | <span data-ttu-id="7ad09-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7ad09-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad09-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ad09-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad09-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ad09-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ad09-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ad09-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad09-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ad09-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ad09-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ad09-138">Namespace</span></span><br/>                | <span data-ttu-id="7ad09-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7ad09-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ad09-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7ad09-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ad09-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ad09-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ad09-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ad09-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ad09-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ad09-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad09-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ad09-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad09-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="7ad09-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

