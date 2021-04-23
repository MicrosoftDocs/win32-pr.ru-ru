---
description: Описание возможностей связанного Мсвм \_ виртуалсистемманажементсервице.
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Класс Msvm_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342792"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="0e2b5-103">\_Класс мсвм виртуалсистемманажементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="0e2b5-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="0e2b5-104">Описание возможностей связанного [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md).</span><span class="sxs-lookup"><span data-stu-id="0e2b5-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="0e2b5-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e2b5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="0e2b5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0e2b5-107">Members</span></span>

<span data-ttu-id="0e2b5-108">Класс **мсвм \_ виртуалсистемманажементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0e2b5-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0e2b5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e2b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e2b5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e2b5-110">Properties</span></span>

<span data-ttu-id="0e2b5-111">Класс **мсвм \_ виртуалсистемманажементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e2b5-112">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-113">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0e2b5-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемманажементкапабилитиес. асинчронаусмесодссуппортед")</span><span class="sxs-lookup"><span data-stu-id="0e2b5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-116">Указывает методы [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) , которые поддерживаются асинхронно в реализации.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e2b5-117">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="0e2b5-118">**[**Валидатепланнедсистем**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="0e2b5-119">**[**Импортсистемдефинитион**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="0e2b5-120">**[**Импортснапшотдефинитионс**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="0e2b5-121">**[**Реализепланнедсистем**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="0e2b5-122">**[**Експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-123">**[**Аддфеатуресеттингс**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-124">**[**Модифифеатуресеттингс**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-125">**[**Ремовефеатуресеттингс**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="0e2b5-126">**[**Жетвиртуалсистемсумбнаилимаже**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="0e2b5-127">**[**Модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="0e2b5-128">**[**Жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="0e2b5-129">**[**Аддквпитемс**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="0e2b5-130">**[**Модификвпитемс**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="0e2b5-131">**[**Ремовеквпитемс**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="0e2b5-132">**[**Форматеррор**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="0e2b5-133">**Рекуестстатечанжесуппортед** (32789)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="0e2b5-134">**Стартсервицесуппортед** (32790)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="0e2b5-135">**Стопсервицесуппортед** (32791)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="0e2b5-136">**[**Модифидискмержесеттингс**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="0e2b5-137">**[**Женератеввпн**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="0e2b5-138">**[**Аддфибречаннелчап**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="0e2b5-139">**[**Ремовефибречаннелчап**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="0e2b5-140">**[**Сетгуестнетворкадаптерконфигуратион**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="0e2b5-141">**[**Жетсизеофсистемфилес**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="0e2b5-142">**[**Жеткуррентввпнфромженератор**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e2b5-143">**Поставщик зарезервирован** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e2b5-144">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-147">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-147">A short description of the object.</span></span> <span data-ttu-id="0e2b5-148">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e2b5-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-152">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-152">A description of the object.</span></span> <span data-ttu-id="0e2b5-153">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e2b5-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-157">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-157">A display name for the object.</span></span> <span data-ttu-id="0e2b5-158">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e2b5-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-159">**елементнамидитсуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-160">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-162">Указывает, можно ли изменить свойство **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="0e2b5-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="0e2b5-163">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-164">**елементнамемаск**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-167">Задает ограничения для **ElementName**, выраженные в виде регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="0e2b5-168">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-169">**индикатионссуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-170">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0e2b5-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-172">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемманажементкапабилитиес. индикатионссуппортед")</span><span class="sxs-lookup"><span data-stu-id="0e2b5-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-173">Указывает события, поддерживаемые реализацией.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="0e2b5-174">Перечисление идентификаторов индикации, которые идентифицируют указание, которое поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="0e2b5-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**Виртуалресаурцестатечанжеиндикатионссуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e2b5-176">Реализация поддерживает уведомления об изменениях состояния экземпляров [**CIM, \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) представляющих ресурсы виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="0e2b5-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**Конкретежобстатечанжеиндикатионссуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e2b5-178">Реализация поддерживает уведомления об изменениях состояния экземпляров [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e2b5-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="0e2b5-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**Виртуалсистемстатечанжеиндикатионссуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e2b5-180">Реализация поддерживает уведомления об изменениях состояния экземпляров [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющих виртуальные системы.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e2b5-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e2b5-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e2b5-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-186">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-187">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0e2b5-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e2b5-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-189">**макселементнамелен**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-190">Тип данных: **unit16**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-192">Квалификаторы: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-193">Задает максимальную поддерживаемую длину свойства **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="0e2b5-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="0e2b5-194">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="0e2b5-195">**рекуестедстатессуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-196">Тип данных: массив **unit16**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-198">Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="0e2b5-199">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="0e2b5-200">Значение</span><span class="sxs-lookup"><span data-stu-id="0e2b5-200">Value</span></span>                                                                         | <span data-ttu-id="0e2b5-201">Значение</span><span class="sxs-lookup"><span data-stu-id="0e2b5-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="0e2b5-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-203">Активировано</span><span class="sxs-lookup"><span data-stu-id="0e2b5-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="0e2b5-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-205">Отключит</span><span class="sxs-lookup"><span data-stu-id="0e2b5-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="0e2b5-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-207">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="0e2b5-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="0e2b5-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-209">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="0e2b5-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="0e2b5-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-211">Тест</span><span class="sxs-lookup"><span data-stu-id="0e2b5-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="0e2b5-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-213">Которого</span><span class="sxs-lookup"><span data-stu-id="0e2b5-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="0e2b5-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="0e2b5-215">Замораживани</span><span class="sxs-lookup"><span data-stu-id="0e2b5-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="0e2b5-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="0e2b5-217">Перезагрузка</span><span class="sxs-lookup"><span data-stu-id="0e2b5-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="0e2b5-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="0e2b5-219">Reset</span><span class="sxs-lookup"><span data-stu-id="0e2b5-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="0e2b5-220">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-221">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0e2b5-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-223">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемманажементкапабилитиес. синчронаусмесодссуппортед")</span><span class="sxs-lookup"><span data-stu-id="0e2b5-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-224">Указывает методы [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) , которые поддерживаются синхронно в реализации.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e2b5-225">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="0e2b5-226">**[**Валидатепланнедсистем**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="0e2b5-227">**[**Импортсистемдефинитион**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="0e2b5-228">**[**Импортснапшотдефинитионс**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="0e2b5-229">**[**Реализепланнедсистем**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="0e2b5-230">**[**Експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-231">**[**Аддфеатуресеттингс**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-232">**[**Модифифеатуресеттингс**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="0e2b5-233">**[**Ремовефеатуресеттингс**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="0e2b5-234">**[**Жетвиртуалсистемсумбнаилимаже**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="0e2b5-235">**[**Модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="0e2b5-236">**[**Жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="0e2b5-237">**[**Аддквпитемс**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="0e2b5-238">**[**Модификвпитемс**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="0e2b5-239">**[**Ремовеквпитемс**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="0e2b5-240">**[**Форматеррор**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="0e2b5-241">**Рекуестстатечанжесуппортед** (32789)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="0e2b5-242">**Стартсервицесуппортед** (32790)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="0e2b5-243">**Стопсервицесуппортед** (32791)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="0e2b5-244">**[**Модифидискмержесеттингс**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="0e2b5-245">**[**Женератеввпн**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="0e2b5-246">**[**Аддфибречаннелчап**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="0e2b5-247">**[**Ремовефибречаннелчап**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="0e2b5-248">**[**Сетгуестнетворкадаптерконфигуратион**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="0e2b5-249">**[**Жетсизеофсистемфилес**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="0e2b5-250">**[**Жеткуррентввпнфромженератор**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e2b5-251">**Поставщик зарезервирован** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e2b5-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e2b5-252">**виртуалсистемтипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2b5-253">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0e2b5-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e2b5-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e2b5-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e2b5-255">Массив строк, каждый из которых указывает тип виртуальной системы, поддерживаемой реализацией.</span><span class="sxs-lookup"><span data-stu-id="0e2b5-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="0e2b5-256">Значение каждого элемента массива, отличного от **null** , должно соответствовать строкам, определенным для свойства [**Мсвм \_ виртуалсистемсеттингдата. виртуалсистемтипе**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2b5-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e2b5-257">Требования</span><span class="sxs-lookup"><span data-stu-id="0e2b5-257">Requirements</span></span>



| <span data-ttu-id="0e2b5-258">Требование</span><span class="sxs-lookup"><span data-stu-id="0e2b5-258">Requirement</span></span> | <span data-ttu-id="0e2b5-259">Значение</span><span class="sxs-lookup"><span data-stu-id="0e2b5-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2b5-260">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e2b5-260">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2b5-261">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0e2b5-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e2b5-262">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e2b5-262">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2b5-263">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0e2b5-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e2b5-264">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e2b5-264">Namespace</span></span><br/>                | <span data-ttu-id="0e2b5-265">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0e2b5-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e2b5-266">MOF</span><span class="sxs-lookup"><span data-stu-id="0e2b5-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e2b5-267"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e2b5-268">DLL</span><span class="sxs-lookup"><span data-stu-id="0e2b5-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e2b5-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e2b5-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

