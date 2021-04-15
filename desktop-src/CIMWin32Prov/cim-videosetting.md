---
description: Класс CIM \_ видеосеттинг связывает \_ объект параметра CIM видеоконтроллерресолутион с контроллером, к которому он применяется.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: Класс CIM_VideoSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656044"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="d00f9-103">\_Класс CIM видеосеттинг</span><span class="sxs-lookup"><span data-stu-id="d00f9-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="d00f9-104">Класс **CIM \_ видеосеттинг** связывает объект параметра [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) с контроллером, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="d00f9-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d00f9-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d00f9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d00f9-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d00f9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d00f9-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d00f9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d00f9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d00f9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00f9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d00f9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="d00f9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d00f9-110">Members</span></span>

<span data-ttu-id="d00f9-111">Класс **CIM \_ видеосеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d00f9-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d00f9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d00f9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d00f9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d00f9-113">Properties</span></span>

<span data-ttu-id="d00f9-114">Класс **CIM \_ видеосеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d00f9-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d00f9-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d00f9-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d00f9-116">Тип данных: **CIM \_ Видеоконтроллер**</span><span class="sxs-lookup"><span data-stu-id="d00f9-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="d00f9-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d00f9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d00f9-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент")</span><span class="sxs-lookup"><span data-stu-id="d00f9-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="d00f9-119">[**\_ Видеоконтроллер CIM**](cim-videocontroller.md) , описывающий видеоконтроллер.</span><span class="sxs-lookup"><span data-stu-id="d00f9-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="d00f9-120">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="d00f9-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d00f9-121">Тип данных: **CIM \_ видеоконтроллерресолутион**</span><span class="sxs-lookup"><span data-stu-id="d00f9-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="d00f9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d00f9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d00f9-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("параметр")</span><span class="sxs-lookup"><span data-stu-id="d00f9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="d00f9-124">[**\_ Видеоконтроллерресолутион CIM**](cim-videocontrollerresolution.md) , описывающий разрешения, частоту обновления, режим сканирования и число цветов, которые могут быть установлены для контроллера.</span><span class="sxs-lookup"><span data-stu-id="d00f9-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d00f9-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d00f9-125">Remarks</span></span>

<span data-ttu-id="d00f9-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d00f9-126">WMI does not implement this class.</span></span> <span data-ttu-id="d00f9-127">Классы WMI, производные от **CIM \_ видеосеттинг**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d00f9-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d00f9-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d00f9-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d00f9-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d00f9-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00f9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d00f9-130">Requirements</span></span>



| <span data-ttu-id="d00f9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d00f9-131">Requirement</span></span> | <span data-ttu-id="d00f9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d00f9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d00f9-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d00f9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d00f9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d00f9-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d00f9-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d00f9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d00f9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d00f9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d00f9-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d00f9-137">Namespace</span></span><br/>                | <span data-ttu-id="d00f9-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d00f9-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d00f9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d00f9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d00f9-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d00f9-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d00f9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d00f9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d00f9-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d00f9-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00f9-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d00f9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00f9-144">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="d00f9-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

