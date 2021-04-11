---
description: '\_Абстрактный класс WMI Комсеттинг Win32 представляет параметры, связанные с компонентом модели COM или COM-приложением.'
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Класс Win32_COMSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262555"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="17fd5-103">\_Класс Win32 комсеттинг</span><span class="sxs-lookup"><span data-stu-id="17fd5-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="17fd5-104">Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ комсеттинг Win32** представляет параметры, связанные с компонентом модели COM или COM-приложением.</span><span class="sxs-lookup"><span data-stu-id="17fd5-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="17fd5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="17fd5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="17fd5-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="17fd5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fd5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17fd5-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="17fd5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="17fd5-108">Members</span></span>

<span data-ttu-id="17fd5-109">Класс **Win32 \_ комсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="17fd5-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="17fd5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="17fd5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17fd5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="17fd5-111">Properties</span></span>

<span data-ttu-id="17fd5-112">Класс **Win32 \_ комсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="17fd5-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17fd5-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="17fd5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fd5-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17fd5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fd5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fd5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fd5-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="17fd5-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="17fd5-117">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="17fd5-117">Short textual description of the current object.</span></span>

<span data-ttu-id="17fd5-118">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="17fd5-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fd5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="17fd5-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fd5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17fd5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fd5-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fd5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17fd5-122">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="17fd5-122">Textual description of the current object.</span></span>

<span data-ttu-id="17fd5-123">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="17fd5-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fd5-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="17fd5-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fd5-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17fd5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fd5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fd5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fd5-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17fd5-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17fd5-128">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="17fd5-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="17fd5-129">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="17fd5-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17fd5-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17fd5-130">Remarks</span></span>

<span data-ttu-id="17fd5-131">Класс **Win32 \_ комсеттинг** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="17fd5-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17fd5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="17fd5-132">Requirements</span></span>



| <span data-ttu-id="17fd5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="17fd5-133">Requirement</span></span> | <span data-ttu-id="17fd5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="17fd5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17fd5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17fd5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="17fd5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17fd5-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17fd5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17fd5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="17fd5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17fd5-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17fd5-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17fd5-139">Namespace</span></span><br/>                | <span data-ttu-id="17fd5-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17fd5-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17fd5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="17fd5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17fd5-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17fd5-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17fd5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="17fd5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17fd5-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fd5-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fd5-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17fd5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fd5-146">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="17fd5-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="17fd5-147">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17fd5-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

