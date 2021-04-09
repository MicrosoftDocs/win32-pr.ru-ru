---
description: Описывает основную поверхность рисования на контроллере экрана.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Класс Msvm_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155166"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="4777b-103">\_Класс мсвм видеохеад</span><span class="sxs-lookup"><span data-stu-id="4777b-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="4777b-104">Описывает основную поверхность рисования на контроллере экрана.</span><span class="sxs-lookup"><span data-stu-id="4777b-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="4777b-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4777b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4777b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4777b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="4777b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4777b-107">Members</span></span>

<span data-ttu-id="4777b-108">Класс **мсвм \_ видеохеад** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4777b-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="4777b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4777b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4777b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4777b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4777b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="4777b-111">Methods</span></span>

<span data-ttu-id="4777b-112">Класс **мсвм \_ видеохеад** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4777b-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="4777b-113">Метод</span><span class="sxs-lookup"><span data-stu-id="4777b-113">Method</span></span>                                                          | <span data-ttu-id="4777b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4777b-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="4777b-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="4777b-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="4777b-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4777b-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="4777b-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="4777b-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4777b-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="4777b-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="4777b-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="4777b-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="4777b-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="4777b-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="4777b-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="4777b-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="4777b-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="4777b-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="4777b-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="4777b-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="4777b-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="4777b-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4777b-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="4777b-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="4777b-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4777b-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4777b-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="4777b-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4777b-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4777b-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="4777b-131">Properties</span></span>

<span data-ttu-id="4777b-132">Класс **мсвм \_ видеохеад** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4777b-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4777b-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="4777b-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4777b-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="4777b-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="4777b-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="4777b-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-141">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-141">The primary availability and status of the device.</span></span> <span data-ttu-id="4777b-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4777b-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="4777b-143">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-143">Value</span></span>                                                                        | <span data-ttu-id="4777b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4777b-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="4777b-146">Не применимо</span><span class="sxs-lookup"><span data-stu-id="4777b-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4777b-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="4777b-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4777b-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4777b-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4777b-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-152">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4777b-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-155">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4777b-155">A short description of the object.</span></span> <span data-ttu-id="4777b-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-157">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="4777b-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-160">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="4777b-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4777b-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4777b-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4777b-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4777b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4777b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="4777b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="4777b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="4777b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="4777b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4777b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4777b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4777b-170">)</span><span class="sxs-lookup"><span data-stu-id="4777b-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4777b-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4777b-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-174">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4777b-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4777b-175">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4777b-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-176">**куррентбитсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="4777b-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-179">Квалификаторы: **единицы** ("биты")</span><span class="sxs-lookup"><span data-stu-id="4777b-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-180">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="4777b-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="4777b-181">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-182">**курренсоризонталресолутион**</span><span class="sxs-lookup"><span data-stu-id="4777b-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-185">Квалификаторы: **единицы** ("Пиксели")</span><span class="sxs-lookup"><span data-stu-id="4777b-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-186">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="4777b-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="4777b-187">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-188">**куррентнумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="4777b-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-189">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4777b-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-191">Число цветов, поддерживаемое в текущих разрешениях.</span><span class="sxs-lookup"><span data-stu-id="4777b-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="4777b-192">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-193">**куррентнумберофколумнс**</span><span class="sxs-lookup"><span data-stu-id="4777b-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-194">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-196">Если в символьном режиме, число столбцов для этого контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="4777b-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="4777b-197">В противном случае флагу присваивается значение 0.</span><span class="sxs-lookup"><span data-stu-id="4777b-197">Otherwise, 0.</span></span> <span data-ttu-id="4777b-198">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-199">**куррентнумберофровс**</span><span class="sxs-lookup"><span data-stu-id="4777b-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-200">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-202">Если в символьном режиме, число строк для этого видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="4777b-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="4777b-203">В противном случае флагу присваивается значение 0.</span><span class="sxs-lookup"><span data-stu-id="4777b-203">Otherwise, 0.</span></span> <span data-ttu-id="4777b-204">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-205">**куррентрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="4777b-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-206">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-208">Квалификаторы: **единицы** ("Герц")</span><span class="sxs-lookup"><span data-stu-id="4777b-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-209">Текущая частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="4777b-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="4777b-210">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-211">**куррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="4777b-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-214">Текущий режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="4777b-214">The current scan mode.</span></span> <span data-ttu-id="4777b-215">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="4777b-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4777b-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4777b-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="4777b-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Операция без чередования** (3)</span><span class="sxs-lookup"><span data-stu-id="4777b-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Операция чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="4777b-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4777b-221">**куррентвертикалресолутион**</span><span class="sxs-lookup"><span data-stu-id="4777b-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-222">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-224">Квалификаторы: **единицы** ("Пиксели")</span><span class="sxs-lookup"><span data-stu-id="4777b-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-225">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="4777b-225">The current number of vertical pixels.</span></span> <span data-ttu-id="4777b-226">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-227">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4777b-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-230">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4777b-230">A description of the object.</span></span> <span data-ttu-id="4777b-231">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4777b-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-233">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-235">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="4777b-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4777b-236">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4777b-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4777b-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4777b-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="4777b-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="4777b-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="4777b-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="4777b-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="4777b-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="4777b-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4777b-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4777b-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4777b-246">)</span><span class="sxs-lookup"><span data-stu-id="4777b-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4777b-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4777b-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-250">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение "Microsoft:*GUID* \\ head \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="4777b-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="4777b-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4777b-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-254">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="4777b-254">A display name for the object.</span></span> <span data-ttu-id="4777b-255">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-256">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="4777b-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-259">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4777b-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4777b-260">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="4777b-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="4777b-261">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-261">Value</span></span>                                                                        | <span data-ttu-id="4777b-262">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4777b-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4777b-264">Активировано</span><span class="sxs-lookup"><span data-stu-id="4777b-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="4777b-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4777b-266">Выключено</span><span class="sxs-lookup"><span data-stu-id="4777b-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4777b-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4777b-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-270">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4777b-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4777b-271">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="4777b-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4777b-272">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4777b-273">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-273">Value</span></span>                                                                        | <span data-ttu-id="4777b-274">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4777b-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4777b-276">Активировано</span><span class="sxs-lookup"><span data-stu-id="4777b-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="4777b-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4777b-278">Выключено</span><span class="sxs-lookup"><span data-stu-id="4777b-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4777b-279">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="4777b-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-280">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4777b-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-282">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="4777b-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="4777b-283">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4777b-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-287">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="4777b-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="4777b-288">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4777b-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-290">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-292">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="4777b-292">The current health of the element.</span></span> <span data-ttu-id="4777b-293">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="4777b-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4777b-294">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="4777b-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4777b-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="4777b-296">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-296">Value</span></span>                                                                        | <span data-ttu-id="4777b-297">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="4777b-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="4777b-299">ОК</span><span class="sxs-lookup"><span data-stu-id="4777b-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4777b-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4777b-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-301">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4777b-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-303">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="4777b-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="4777b-304">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4777b-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-306">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4777b-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-308">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4777b-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4777b-309">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4777b-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-313">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="4777b-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4777b-314">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="4777b-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4777b-315">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-316">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="4777b-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-317">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-319">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="4777b-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="4777b-320">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-321">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="4777b-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-322">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4777b-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-324">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4777b-324">This property has been deprecated.</span></span> <span data-ttu-id="4777b-325">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4777b-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-326">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="4777b-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-327">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-329">Квалификаторы: **единицы** ("Герц")</span><span class="sxs-lookup"><span data-stu-id="4777b-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-330">Максимальная частота обновления контроллера экрана в герцах.</span><span class="sxs-lookup"><span data-stu-id="4777b-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="4777b-331">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-332">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="4777b-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-333">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4777b-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4777b-335">Квалификаторы: **единицы** ("Герц")</span><span class="sxs-lookup"><span data-stu-id="4777b-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="4777b-336">Минимальная частота обновления видеоконтроллера (в герцах).</span><span class="sxs-lookup"><span data-stu-id="4777b-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="4777b-337">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-338">**Name**</span><span class="sxs-lookup"><span data-stu-id="4777b-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-341">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="4777b-341">The label by which the object is known.</span></span> <span data-ttu-id="4777b-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="4777b-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-343">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="4777b-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-346">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4777b-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4777b-347">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4777b-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4777b-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4777b-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4777b-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="4777b-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="4777b-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="4777b-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="4777b-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="4777b-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="4777b-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="4777b-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="4777b-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="4777b-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="4777b-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="4777b-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="4777b-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="4777b-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="4777b-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="4777b-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="4777b-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4777b-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4777b-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4777b-368">)</span><span class="sxs-lookup"><span data-stu-id="4777b-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4777b-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4777b-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4777b-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-372">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="4777b-372">The current statuses of the object.</span></span> <span data-ttu-id="4777b-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-374">**осеркуррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="4777b-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-375">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-377">Текущий режим просмотра, когда свойство **куррентсканмоде** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="4777b-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="4777b-378">Это свойство наследуется от [**CIM \_ видеохеад**](/previous-versions//cc136948(v=vs.85)) и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-379">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="4777b-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-382">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="4777b-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4777b-383">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="4777b-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4777b-384">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4777b-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-386">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4777b-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-388">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4777b-389">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-390">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="4777b-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-391">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4777b-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-393">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-393">The power management capabilities of the device.</span></span> <span data-ttu-id="4777b-394">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-395">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="4777b-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-396">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4777b-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-398">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4777b-399">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-400">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="4777b-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-401">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4777b-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-403">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="4777b-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4777b-404">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-405">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="4777b-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-406">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-408">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="4777b-408">Provides high level status information.</span></span> <span data-ttu-id="4777b-409">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="4777b-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4777b-410">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4777b-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4777b-411">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4777b-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4777b-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-413"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="4777b-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="4777b-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="4777b-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4777b-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4777b-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4777b-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4777b-418">)</span><span class="sxs-lookup"><span data-stu-id="4777b-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4777b-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4777b-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-420">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-422">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="4777b-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="4777b-423">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="4777b-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4777b-424">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4777b-425">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-425">Value</span></span>                                                                         | <span data-ttu-id="4777b-426">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4777b-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4777b-428">Не применимо</span><span class="sxs-lookup"><span data-stu-id="4777b-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4777b-429">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="4777b-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-432">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="4777b-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="4777b-433">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-434">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="4777b-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-435">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4777b-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4777b-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-437">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4777b-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4777b-438">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4777b-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4777b-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-440">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-442">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4777b-442">The current state of the logical device.</span></span> <span data-ttu-id="4777b-443">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-444">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="4777b-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-447">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="4777b-447">The scoping system's creation class name.</span></span> <span data-ttu-id="4777b-448">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4777b-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4777b-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-450">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4777b-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-452">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4777b-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="4777b-453">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4777b-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4777b-454">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="4777b-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-455">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4777b-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-457">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4777b-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4777b-458">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4777b-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-459">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="4777b-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-460">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4777b-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-462">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="4777b-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4777b-463">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="4777b-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4777b-464">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="4777b-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4777b-465">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4777b-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4777b-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4777b-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4777b-467">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4777b-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4777b-468">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4777b-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4777b-469">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-469">Value</span></span>                                                                         | <span data-ttu-id="4777b-470">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4777b-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4777b-472">Не применимо</span><span class="sxs-lookup"><span data-stu-id="4777b-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4777b-473">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4777b-473">Remarks</span></span>

<span data-ttu-id="4777b-474">Доступ к классу **\_ видеохеад мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4777b-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4777b-475">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4777b-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4777b-476">Требования</span><span class="sxs-lookup"><span data-stu-id="4777b-476">Requirements</span></span>



| <span data-ttu-id="4777b-477">Требование</span><span class="sxs-lookup"><span data-stu-id="4777b-477">Requirement</span></span> | <span data-ttu-id="4777b-478">Значение</span><span class="sxs-lookup"><span data-stu-id="4777b-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4777b-479">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4777b-479">Minimum supported client</span></span><br/> | <span data-ttu-id="4777b-480">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4777b-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4777b-481">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4777b-481">Minimum supported server</span></span><br/> | <span data-ttu-id="4777b-482">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4777b-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4777b-483">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4777b-483">Namespace</span></span><br/>                | <span data-ttu-id="4777b-484">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4777b-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4777b-485">MOF</span><span class="sxs-lookup"><span data-stu-id="4777b-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4777b-486"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4777b-487">DLL</span><span class="sxs-lookup"><span data-stu-id="4777b-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4777b-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4777b-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4777b-489">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4777b-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4777b-490">**\_ВИДЕОХЕАД CIM**</span><span class="sxs-lookup"><span data-stu-id="4777b-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="4777b-491">[**\_ВИДЕОХЕАД CIM**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4777b-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4777b-492">Классы видео</span><span class="sxs-lookup"><span data-stu-id="4777b-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

