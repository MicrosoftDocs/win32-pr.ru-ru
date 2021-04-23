---
description: '\_Класс WMI ауточксеттинг для Win32 представляет параметры для операции Автопроверки диска.'
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Класс Win32_AutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656027"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="7eb64-103">\_Класс Win32 ауточксеттинг</span><span class="sxs-lookup"><span data-stu-id="7eb64-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="7eb64-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ауточксеттинг для Win32** представляет параметры для операции Автопроверки диска.</span><span class="sxs-lookup"><span data-stu-id="7eb64-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="7eb64-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7eb64-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7eb64-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7eb64-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb64-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eb64-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="7eb64-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7eb64-108">Members</span></span>

<span data-ttu-id="7eb64-109">Класс **Win32 \_ ауточксеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7eb64-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="7eb64-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7eb64-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eb64-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7eb64-111">Properties</span></span>

<span data-ttu-id="7eb64-112">Класс **Win32 \_ ауточксеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7eb64-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eb64-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7eb64-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb64-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7eb64-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7eb64-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7eb64-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eb64-117">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7eb64-117">Short textual description of the current object.</span></span>

<span data-ttu-id="7eb64-118">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7eb64-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb64-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7eb64-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb64-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7eb64-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7eb64-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eb64-122">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7eb64-122">Textual description of the current object.</span></span>

<span data-ttu-id="7eb64-123">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7eb64-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb64-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7eb64-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb64-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7eb64-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7eb64-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("свойство settingid"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7eb64-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7eb64-128">Идентификатор, который используется как часть ключа для текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7eb64-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="7eb64-129">**усеринпутделай**</span><span class="sxs-lookup"><span data-stu-id="7eb64-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb64-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eb64-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7eb64-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7eb64-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| ауточктимеаут"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds")</span><span class="sxs-lookup"><span data-stu-id="7eb64-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="7eb64-133">Задержка ввода данных пользователем для Автопроверки.</span><span class="sxs-lookup"><span data-stu-id="7eb64-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eb64-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7eb64-134">Remarks</span></span>

<span data-ttu-id="7eb64-135">Класс **Win32 \_ ауточксеттинг** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7eb64-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb64-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7eb64-136">Requirements</span></span>



| <span data-ttu-id="7eb64-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7eb64-137">Requirement</span></span> | <span data-ttu-id="7eb64-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7eb64-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb64-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7eb64-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb64-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eb64-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7eb64-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7eb64-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb64-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eb64-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7eb64-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7eb64-143">Namespace</span></span><br/>                | <span data-ttu-id="7eb64-144">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7eb64-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7eb64-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7eb64-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eb64-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eb64-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eb64-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7eb64-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eb64-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eb64-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb64-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7eb64-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb64-150">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="7eb64-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7eb64-151">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7eb64-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

