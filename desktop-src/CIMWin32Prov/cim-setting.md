---
description: '\_Класс параметров CIM представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.'
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: Класс CIM_Setting (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895789"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="cdb8f-103">Класс CIM_Setting (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cdb8f-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cdb8f-104">Класс **\_ параметров CIM** представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="cdb8f-105">С управляемым системным элементом может быть связано несколько объектов параметров.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="cdb8f-106">Текущие рабочие значения для параметров элемента отражаются свойствами в самом элементе или свойствами в его связях.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="cdb8f-107">Эти свойства не обязательно должны совпадать со значениями, присутствующими в объекте Setting.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="cdb8f-108">Например, у модема может быть значение скорости в 56 КБ в секунду, но оно должно работать с 19,2 килобайт в секунду.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdb8f-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cdb8f-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cdb8f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cdb8f-111">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cdb8f-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb8f-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdb8f-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="cdb8f-114">Члены</span><span class="sxs-lookup"><span data-stu-id="cdb8f-114">Members</span></span>

<span data-ttu-id="cdb8f-115">Класс **\_ параметров CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdb8f-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="cdb8f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdb8f-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdb8f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdb8f-117">Properties</span></span>

<span data-ttu-id="cdb8f-118">Класс **\_ параметров CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdb8f-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb8f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb8f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdb8f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdb8f-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cdb8f-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cdb8f-123">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="cdb8f-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb8f-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb8f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdb8f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdb8f-127">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="cdb8f-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb8f-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdb8f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb8f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdb8f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdb8f-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cdb8f-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cdb8f-132">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdb8f-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdb8f-133">Remarks</span></span>

<span data-ttu-id="cdb8f-134">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-134">WMI does not implement this class.</span></span> <span data-ttu-id="cdb8f-135">Классы WMI, производные **от \_ параметра CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cdb8f-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cdb8f-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cdb8f-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cdb8f-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb8f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="cdb8f-138">Requirements</span></span>



| <span data-ttu-id="cdb8f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="cdb8f-139">Requirement</span></span> | <span data-ttu-id="cdb8f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="cdb8f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb8f-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdb8f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb8f-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdb8f-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdb8f-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdb8f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb8f-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdb8f-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdb8f-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdb8f-145">Namespace</span></span><br/>                | <span data-ttu-id="cdb8f-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cdb8f-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cdb8f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cdb8f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdb8f-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdb8f-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdb8f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cdb8f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdb8f-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdb8f-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

