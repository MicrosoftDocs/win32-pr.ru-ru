---
description: '\_Класс WMI взаимосвязей Win32 видеосеттингс связывает видеоконтроллер и параметры видео, которые можно применить к нему.'
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Класс Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655744"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="68467-103">\_Класс Win32 видеосеттингс</span><span class="sxs-lookup"><span data-stu-id="68467-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="68467-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ видеосеттингс** связывает видеоконтроллер и параметры видео, которые можно применить к нему.</span><span class="sxs-lookup"><span data-stu-id="68467-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="68467-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="68467-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68467-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="68467-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68467-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68467-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="68467-108">Члены</span><span class="sxs-lookup"><span data-stu-id="68467-108">Members</span></span>

<span data-ttu-id="68467-109">Класс **Win32 \_ видеосеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68467-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="68467-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="68467-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68467-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="68467-111">Properties</span></span>

<span data-ttu-id="68467-112">Класс **Win32 \_ видеосеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="68467-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68467-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="68467-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68467-114">Тип данных: **Win32 \_ Видеоконтроллер**</span><span class="sxs-lookup"><span data-stu-id="68467-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="68467-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68467-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68467-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Видеоконтроллер")</span><span class="sxs-lookup"><span data-stu-id="68467-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="68467-117">[**\_ Видеоконтроллер Win32**](win32-videocontroller.md) , содержащий свойства видеоконтроллера, на котором можно использовать параметр видео.</span><span class="sxs-lookup"><span data-stu-id="68467-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="68467-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="68467-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68467-119">Тип данных: **CIM \_ видеоконтроллерресолутион**</span><span class="sxs-lookup"><span data-stu-id="68467-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="68467-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68467-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68467-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ видеоконтроллерресолутион")</span><span class="sxs-lookup"><span data-stu-id="68467-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="68467-122">[**\_ Видеоконтроллерресолутион CIM**](cim-videocontrollerresolution.md) , содержащий параметры, которые можно применить к видеоконтроллеру.</span><span class="sxs-lookup"><span data-stu-id="68467-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68467-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68467-123">Remarks</span></span>

<span data-ttu-id="68467-124">Класс **Win32 \_ видеосеттингс** является производным от [**CIM \_ видеосеттинг**](cim-videosetting.md).</span><span class="sxs-lookup"><span data-stu-id="68467-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68467-125">Требования</span><span class="sxs-lookup"><span data-stu-id="68467-125">Requirements</span></span>



| <span data-ttu-id="68467-126">Требование</span><span class="sxs-lookup"><span data-stu-id="68467-126">Requirement</span></span> | <span data-ttu-id="68467-127">Значение</span><span class="sxs-lookup"><span data-stu-id="68467-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68467-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68467-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68467-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68467-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68467-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68467-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68467-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68467-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68467-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68467-132">Namespace</span></span><br/>                | <span data-ttu-id="68467-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68467-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68467-134">MOF</span><span class="sxs-lookup"><span data-stu-id="68467-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68467-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68467-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68467-136">DLL</span><span class="sxs-lookup"><span data-stu-id="68467-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68467-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68467-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68467-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68467-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68467-139">**\_ВИДЕОСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="68467-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="68467-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="68467-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
