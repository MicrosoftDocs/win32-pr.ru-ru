---
description: '\_Класс WMI взаимосвязей Win32 пажефилилементсеттинг связывает начальные параметры файла подкачки и состояние этих параметров во время нормальной работы.'
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Класс Win32_PageFileElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990726"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="718fa-103">\_Класс Win32 пажефилилементсеттинг</span><span class="sxs-lookup"><span data-stu-id="718fa-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="718fa-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ пажефилилементсеттинг** связывает начальные параметры файла подкачки и состояние этих параметров во время нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="718fa-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="718fa-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="718fa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="718fa-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="718fa-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="718fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="718fa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="718fa-108">Члены</span><span class="sxs-lookup"><span data-stu-id="718fa-108">Members</span></span>

<span data-ttu-id="718fa-109">Класс **Win32 \_ пажефилилементсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="718fa-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="718fa-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="718fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="718fa-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="718fa-111">Properties</span></span>

<span data-ttu-id="718fa-112">Класс **Win32 \_ пажефилилементсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="718fa-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="718fa-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="718fa-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="718fa-114">Тип данных: **Win32 \_ пажефилеусаже**</span><span class="sxs-lookup"><span data-stu-id="718fa-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="718fa-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="718fa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="718fa-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пажефилеусаже")</span><span class="sxs-lookup"><span data-stu-id="718fa-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="718fa-117">Ссылка на экземпляр, представляющий свойства файла подкачки во время использования системы Win32.</span><span class="sxs-lookup"><span data-stu-id="718fa-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="718fa-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="718fa-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="718fa-119">Тип данных: **Win32 \_ пажефилесеттинг**</span><span class="sxs-lookup"><span data-stu-id="718fa-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="718fa-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="718fa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="718fa-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пажефилесеттинг")</span><span class="sxs-lookup"><span data-stu-id="718fa-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="718fa-122">Ссылка на экземпляр, представляющий начальные параметры файла подкачки при запуске системы Win32.</span><span class="sxs-lookup"><span data-stu-id="718fa-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="718fa-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="718fa-123">Remarks</span></span>

<span data-ttu-id="718fa-124">Класс **Win32 \_ пажефилилементсеттинг** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="718fa-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="718fa-125">Требования</span><span class="sxs-lookup"><span data-stu-id="718fa-125">Requirements</span></span>



| <span data-ttu-id="718fa-126">Требование</span><span class="sxs-lookup"><span data-stu-id="718fa-126">Requirement</span></span> | <span data-ttu-id="718fa-127">Значение</span><span class="sxs-lookup"><span data-stu-id="718fa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="718fa-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="718fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="718fa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="718fa-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="718fa-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="718fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="718fa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="718fa-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="718fa-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="718fa-132">Namespace</span></span><br/>                | <span data-ttu-id="718fa-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="718fa-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="718fa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="718fa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="718fa-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="718fa-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="718fa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="718fa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="718fa-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718fa-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="718fa-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="718fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718fa-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="718fa-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="718fa-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="718fa-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
