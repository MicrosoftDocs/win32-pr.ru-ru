---
description: Класс CIM \_ мониторсеттинг связывает разрешение монитора с монитором рабочего стола, к которому он применяется.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: Класс CIM_MonitorSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896093"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="b3db3-103">\_Класс CIM мониторсеттинг</span><span class="sxs-lookup"><span data-stu-id="b3db3-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="b3db3-104">Класс **CIM \_ мониторсеттинг** связывает разрешение монитора с монитором рабочего стола, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="b3db3-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3db3-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b3db3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3db3-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3db3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3db3-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b3db3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3db3-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b3db3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3db3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3db3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="b3db3-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b3db3-110">Members</span></span>

<span data-ttu-id="b3db3-111">Класс **CIM \_ мониторсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b3db3-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="b3db3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b3db3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3db3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b3db3-113">Properties</span></span>

<span data-ttu-id="b3db3-114">Класс **CIM \_ мониторсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b3db3-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3db3-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b3db3-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3db3-116">Тип данных: **CIM \_ десктопмонитор**</span><span class="sxs-lookup"><span data-stu-id="b3db3-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="b3db3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b3db3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3db3-118">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент")</span><span class="sxs-lookup"><span data-stu-id="b3db3-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="b3db3-119">[**\_ Десктопмонитор CIM**](cim-desktopmonitor.md) , описывающий настольный монитор.</span><span class="sxs-lookup"><span data-stu-id="b3db3-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b3db3-120">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="b3db3-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3db3-121">Тип данных: **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="b3db3-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="b3db3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b3db3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3db3-123">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("параметр")</span><span class="sxs-lookup"><span data-stu-id="b3db3-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="b3db3-124">[**\_ MonitorResolution CIM**](cim-monitorresolution.md) , описывающий разрешение монитора, связанное с настольным монитором.</span><span class="sxs-lookup"><span data-stu-id="b3db3-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3db3-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3db3-125">Remarks</span></span>

<span data-ttu-id="b3db3-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b3db3-126">WMI does not implement this class.</span></span>

<span data-ttu-id="b3db3-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b3db3-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3db3-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b3db3-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3db3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b3db3-129">Requirements</span></span>



| <span data-ttu-id="b3db3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b3db3-130">Requirement</span></span> | <span data-ttu-id="b3db3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b3db3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3db3-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3db3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b3db3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3db3-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3db3-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3db3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b3db3-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3db3-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3db3-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b3db3-136">Namespace</span></span><br/>                | <span data-ttu-id="b3db3-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b3db3-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3db3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b3db3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3db3-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3db3-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3db3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b3db3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3db3-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3db3-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3db3-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3db3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3db3-143">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="b3db3-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

