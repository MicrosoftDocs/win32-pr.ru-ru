---
description: Представляет параметры компонента модели COM.
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Класс Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655993"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="0f9c9-103">\_Класс Win32 классиккомкласссеттинг</span><span class="sxs-lookup"><span data-stu-id="0f9c9-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="0f9c9-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ классиккомкласссеттинг для Win32** представляет параметры компонента модели COM.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="0f9c9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0f9c9-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f9c9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="0f9c9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0f9c9-108">Members</span></span>

<span data-ttu-id="0f9c9-109">Класс **Win32 \_ классиккомкласссеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f9c9-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0f9c9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f9c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f9c9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f9c9-111">Properties</span></span>

<span data-ttu-id="0f9c9-112">Класс **Win32 \_ классиккомкласссеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f9c9-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-116">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-117">Глобальный уникальный идентификатор (GUID) для COM-приложения, использующего этот COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-118">**аутоконверттоклсид**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-121">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ аутоконвертто \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-122">Идентификатор GUID класса COM, в который будет автоматически преобразован этот COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-123">**аутотреатасклсид**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-126">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ аутотреатас \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-127">Идентификатор GUID для COM-компонента, который будет автоматически эмулировать экземпляры этого класса.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-128">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0f9c9-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-132">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-132">Short textual description of the current object.</span></span>

<span data-ttu-id="0f9c9-133">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f9c9-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-137">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ по умолчанию \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-138">Идентификатор GUID этого COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-139">**Управление**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-143">Компонент COM является элементом управления OLE.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-144">**дефаултикон**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ дефаултикон \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-148">Путь к исполняемому файлу и идентификатору ресурса значка по умолчанию, используемого классом.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-152">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-152">Textual description of the current object.</span></span>

<span data-ttu-id="0f9c9-153">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f9c9-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-154">**инпрочандлер**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-157">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ инпрочандлер \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-158">Полный путь, включая имя файла или только имя файла для 16-разрядного пользовательского обработчика COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="0f9c9-159">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-163">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-164">Полный путь, включая имя файла или только имя файла для 32-разрядного пользовательского обработчика COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="0f9c9-165">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-166">**инпроксервер**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-169">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ инпроксервер \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-170">Полный путь, включая имя файла или только имя файла для 16-разрядного внутрипроцессного сервера DLL для этого COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="0f9c9-171">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-175">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-176">Полный путь, включая имя файла или только имя файла для 32-разрядного внутрипроцессного сервера DLL для этого COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="0f9c9-177">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-178">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-179">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-181">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ inserted")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-182">Компонент COM можно вставить в приложения-контейнеры OLE.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-183">**жавакласс**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-186">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ жавакласс \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-187">Компонент COM является компонентом Java.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-188">**локалсервер**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-191">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ локалсервер \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-192">Полный путь, включая имя файла или только имя файла для 16-разрядного локального серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="0f9c9-193">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-197">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ по умолчанию \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-198">Полный путь, включая имя файла или только имя файла для 32-битного локального серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="0f9c9-199">Поставщик не всегда возвращает полный путь.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-200">**лонгдисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-203">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ауксусертипе \\ \\ 3 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-204">Полное имя приложения COM.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-204">Full name of the COM application.</span></span> <span data-ttu-id="0f9c9-205">Он используется в таких областях, как поле **результатов** в диалоговом окне « **Специальная вставка OLE** ».</span><span class="sxs-lookup"><span data-stu-id="0f9c9-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-206">**ID**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-209">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ по умолчанию \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-210">Программный идентификатор, связанный с COM-компонентом.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="0f9c9-211">Формат ProgID имеет вид <Vendor. <Component. <версии.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="0f9c9-212">Этот идентификатор не обязательно должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-216">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0f9c9-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-217">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="0f9c9-218">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f9c9-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-222">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ауксусертипе \\ \\ 2 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-223">Короткое имя приложения COM (используется в меню и всплывающих окнах).</span><span class="sxs-lookup"><span data-stu-id="0f9c9-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-227">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-228">Потоковая модель, используемая внутрипроцессный COM-классами.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="0f9c9-229">Если это свойство имеет **значение NULL**, то модель потоков не используется.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="0f9c9-230">Компонент создается в основном потоке клиента, а вызовы из других потоков маршалируются в этот поток.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="0f9c9-231">Модель подразделения указывает, что компоненты могут быть указаны только одним потоком.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="0f9c9-232">Общие данные, удерживаемые этими типами серверов объектов, должны быть защищены от конфликтов потоков, так как объектный сервер поддерживает несколько компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="0f9c9-233">Каждый компонент может быть одновременно задан разными потоками.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="0f9c9-234">Бесплатная модель указывает, что компоненты не накладывают ограничений на то, какие потоки или сколько потоков могут войти в этот объект.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="0f9c9-235">Объект не может содержать данные конкретного потока и должен защищать его данные от одновременного доступа из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="0f9c9-236">Доступ к компонентам с произвольным потоком, однако, не может осуществляться напрямую между апартаментными потоками, а вызовы к ним маршалируются из подразделения клиента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="0f9c9-237">Если заданы оба значения, компоненты можно использовать в режимах с потоковым апартаментом или в свободной потоке.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="0f9c9-238">Эти компоненты могут вводиться несколькими потоками, защищать свои данные от конфликтов потоков и не содержать данные, связанные с потоком.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="0f9c9-239">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="0f9c9-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="0f9c9-240">Разделение</span><span class="sxs-lookup"><span data-stu-id="0f9c9-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="0f9c9-241">Свободный</span><span class="sxs-lookup"><span data-stu-id="0f9c9-241">"Free"</span></span></dd> <dd><span data-ttu-id="0f9c9-242">Как</span><span class="sxs-lookup"><span data-stu-id="0f9c9-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="0f9c9-243">**Подразделение** ("подразделение")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="0f9c9-244">**Бесплатный** ("бесплатный")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="0f9c9-245">**Оба** ("оба")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f9c9-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-249">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-250">Имя модуля и идентификатор ресурса для мелкого (16x16) точечного рисунка, используемого для кнопки панели инструментов или панели элементов.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="0f9c9-251">Используется, если COM-компонент является элементом управления OLE или ActiveX.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-252">**треатасклсид**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-255">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ треатас \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-256">Идентификатор GUID COM-компонента, который может эмулировать экземпляры этого компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-257">**типелибрарид**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-260">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-261">Идентификатор GUID для библиотеки типов для этого COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-265">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ версия \[ по умолчанию \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-266">Номер версии этого COM-класса.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="0f9c9-267">**версиониндепендентпрогид**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9c9-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f9c9-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9c9-270">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ версиониндепендентпрогид \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="0f9c9-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0f9c9-271">Идентификатор программы, который согласуется для всех версий той же программы.</span><span class="sxs-lookup"><span data-stu-id="0f9c9-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f9c9-272">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f9c9-272">Remarks</span></span>

<span data-ttu-id="0f9c9-273">Класс **Win32 \_ классиккомкласссеттинг** является производным от [**Win32 \_ комсеттинг**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="0f9c9-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f9c9-274">Требования</span><span class="sxs-lookup"><span data-stu-id="0f9c9-274">Requirements</span></span>



| <span data-ttu-id="0f9c9-275">Требование</span><span class="sxs-lookup"><span data-stu-id="0f9c9-275">Requirement</span></span> | <span data-ttu-id="0f9c9-276">Значение</span><span class="sxs-lookup"><span data-stu-id="0f9c9-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9c9-277">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f9c9-277">Minimum supported client</span></span><br/> | <span data-ttu-id="0f9c9-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f9c9-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f9c9-279">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f9c9-279">Minimum supported server</span></span><br/> | <span data-ttu-id="0f9c9-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f9c9-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f9c9-281">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f9c9-281">Namespace</span></span><br/>                | <span data-ttu-id="0f9c9-282">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f9c9-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f9c9-283">MOF</span><span class="sxs-lookup"><span data-stu-id="0f9c9-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f9c9-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f9c9-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f9c9-285">DLL</span><span class="sxs-lookup"><span data-stu-id="0f9c9-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f9c9-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f9c9-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9c9-287">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f9c9-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9c9-288">**\_Комсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0f9c9-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="0f9c9-289">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f9c9-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

