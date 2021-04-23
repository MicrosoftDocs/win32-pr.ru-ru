---
description: Представляет службу виртуализации, имеющуюся в одной системе узла.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Класс Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808777"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f0a9f-103">\_Класс мсвм виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="f0a9f-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f0a9f-104">Представляет службу виртуализации, имеющуюся в одной системе узла.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="f0a9f-105">**Мсвм \_ Виртуалсистемманажементсервице** используется для управления определением, изменением и удалением виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="f0a9f-106">Он также содержит методы для выполнения операций на виртуальных машинах, таких как клонирование, значит, импорт или экспорт виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="f0a9f-107">Чтобы получить сведения о виртуальной машине, используйте [**мсвм \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="f0a9f-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a9f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0a9f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="f0a9f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f0a9f-110">Members</span></span>

<span data-ttu-id="f0a9f-111">Класс **мсвм \_ виртуалсистемманажементсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f0a9f-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="f0a9f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f0a9f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f0a9f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0a9f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f0a9f-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f0a9f-114">Methods</span></span>

<span data-ttu-id="f0a9f-115">Класс **мсвм \_ виртуалсистемманажементсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="f0a9f-116">Метод</span><span class="sxs-lookup"><span data-stu-id="f0a9f-116">Method</span></span>                                                                                                                 | <span data-ttu-id="f0a9f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f0a9f-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0a9f-118">**аддбутсаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="f0a9f-119">Добавляет исходные загрузочные источники в конфигурацию виртуальной системы при их применении к конфигурации виртуальной системы "состояние".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="f0a9f-120">**аддфеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="f0a9f-121">Добавляет параметры Ethernet-компонентов в конфигурацию подключения Ethernet виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="f0a9f-122">**аддфибречаннелчап**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="f0a9f-123">Добавляет параметры DH-CHAP в виртуальный порт Fibre Channel виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="f0a9f-124">**аддгуестсервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="f0a9f-125">Добавляет параметры гостевой службы в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="f0a9f-126">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="f0a9f-127">**аддквпитемс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="f0a9f-128">Добавляет пары "ключ-значение" в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="f0a9f-129">**аддресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="f0a9f-130">Добавляет ресурсы в конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="f0a9f-131">**аддсистемкомпонентсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="f0a9f-132">Добавляет универсальные параметры в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="f0a9f-133">**дефинепланнедсистем**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="f0a9f-134">Определяет запланированную виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="f0a9f-135">Входные данные, которые указаны не полностью, могут быть заполнены значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f0a9f-136">**дефинесистем**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="f0a9f-137">Создает новое определение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="f0a9f-138">**дестройсистем**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="f0a9f-139">Удаляет существующее определение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="f0a9f-140">**диагносенетворкконнектион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="f0a9f-141">Диагностика сетевого подключения виртуальной машины в среде виртуализации сети Windows.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="f0a9f-142">**експортсистемдефинитион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="f0a9f-143">Экспортирует виртуальную машину или моментальный снимок виртуальной машины в файл.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="f0a9f-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="f0a9f-145">Возвращает отформатированную строку сообщения об ошибке для указанного массива внедренных экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a9f-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="f0a9f-146">**женератеввпн**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="f0a9f-147">Формирует набор WWN-имен портов (Ввпнс).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="f0a9f-148">**жеткуррентввпнфромженератор**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="f0a9f-149">Предоставляет возможность предварительного просмотра текущего WWN-имени порта (WWPN) без зарезервированного WWPN.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="f0a9f-150">**жетдефинитионфилесуммаринформатион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="f0a9f-151">Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="f0a9f-152">**жетсизеофсистемфилес**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="f0a9f-153">Получает общий размер системных файлов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="f0a9f-154">**жетсуммаринформатион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="f0a9f-155">Возвращает сводные данные о виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="f0a9f-156">**жетвиртуалсистемсумбнаилимаже**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="f0a9f-157">Извлекает эскиз имеющейся виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="f0a9f-158">**импортснапшотдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="f0a9f-159">Ищет в указанной папке файлы определения моментальных снимков, связанные с указанной запланированной системой компьютера, и создает новый моментальный снимок в запланированной компьютерной системе для каждого связанного файла определения в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="f0a9f-160">**импортсистемдефинитион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="f0a9f-161">Создает новую запланированную компьютерную систему на основе указанного определения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="f0a9f-162">**модифидискмержесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="f0a9f-163">Изменяет данные параметров слияния диска.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="f0a9f-164">**модифифеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="f0a9f-165">Изменяет текущие настройки компонентов подключения Ethernet виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="f0a9f-166">**модифигуестсервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="f0a9f-167">Изменяет параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="f0a9f-168">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="f0a9f-169">**модификвпитемс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="f0a9f-170">Изменяет существующие пары "ключ-значение" на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="f0a9f-171">**модифиресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="f0a9f-172">Изменяет параметры виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="f0a9f-173">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="f0a9f-174">Изменяет данные настройки службы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="f0a9f-175">**модифисистемкомпонентсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="f0a9f-176">Изменяет общие параметры системных компонентов.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="f0a9f-177">**модифисистемсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="f0a9f-178">Изменяет параметры виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="f0a9f-179">**реализепланнедсистем**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="f0a9f-180">Проверяет конфигурацию запланированной виртуальной машины и преобразует ее в реализованную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="f0a9f-181">**ремовебутсаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="f0a9f-182">Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="f0a9f-183">При применении к частям "текущей" конфигурации виртуальной системы, так как ресурсы активной виртуальной системы могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="f0a9f-184">**ремовефеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="f0a9f-185">Удаляет параметры компонентов из Ethernet-подключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="f0a9f-186">**ремовефибречаннелчап**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="f0a9f-187">Удаление параметров DH-CHAP из искусственного Fibre Channel порта на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="f0a9f-188">**ремовегуестсервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="f0a9f-189">Удаляет параметры гостевой службы из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="f0a9f-190">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="f0a9f-191">**ремовеквпитемс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="f0a9f-192">Удаляет существующие пары "ключ-значение" из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="f0a9f-193">**ремовересаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="f0a9f-194">Удаляет параметры виртуального ресурса из конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="f0a9f-195">**ремовесистемкомпонентсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="f0a9f-196">Удаляет параметры универсального компонента из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="f0a9f-197">**Равен**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="f0a9f-198">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="f0a9f-199">**сетгуестнетворкадаптерконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="f0a9f-200">Настраивает сетевые адаптеры в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="f0a9f-201">**сетинитиалмачинеконфигуратиондата**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="f0a9f-202">Задает исходные данные конфигурации ВИРТУАЛЬНОЙ машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="f0a9f-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="f0a9f-204">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="f0a9f-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="f0a9f-206">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="f0a9f-207">**тестнетворкконнектион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="f0a9f-208">Проверяет сетевое подключение виртуальной машины в среде виртуализации сети Windows.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="f0a9f-209">**упградесистемверсион**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="f0a9f-210">Обновляет виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="f0a9f-211">При применении к параметрам системы "Текущая" Конфигурация виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="f0a9f-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="f0a9f-212">**валидатепланнедсистем**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="f0a9f-213">Проверяет указанную запланированную систему.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="f0a9f-214">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0a9f-214">Properties</span></span>

<span data-ttu-id="f0a9f-215">Класс **мсвм \_ виртуалсистемманажементсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0a9f-216">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-217">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f0a9f-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-219">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f0a9f-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f0a9f-220">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-221">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-224">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-224">A short description of the object.</span></span> <span data-ttu-id="f0a9f-225">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-226">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-227">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-229">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f0a9f-230">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a9f-231">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f0a9f-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f0a9f-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f0a9f-239">)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a9f-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-243">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-244">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f0a9f-245">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ виртуалсистемманажементсервице".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-246">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-249">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-249">A description of the object.</span></span> <span data-ttu-id="f0a9f-250">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба для создания виртуальных машин и управления ими".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-252">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-254">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f0a9f-255">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a9f-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f0a9f-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f0a9f-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f0a9f-265">)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a9f-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-269">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-269">A display name for the object.</span></span> <span data-ttu-id="f0a9f-270">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-271">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-272">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-274">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f0a9f-275">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="f0a9f-276">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-276">Value</span></span>                                                                        | <span data-ttu-id="f0a9f-277">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="f0a9f-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f0a9f-279">Активировано</span><span class="sxs-lookup"><span data-stu-id="f0a9f-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0a9f-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-281">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-283">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f0a9f-284">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="f0a9f-285">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="f0a9f-286">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-286">Value</span></span>                                                                        | <span data-ttu-id="f0a9f-287">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="f0a9f-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f0a9f-289">Активировано</span><span class="sxs-lookup"><span data-stu-id="f0a9f-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0a9f-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-291">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-293">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-293">The current health of the element.</span></span> <span data-ttu-id="f0a9f-294">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f0a9f-295">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f0a9f-296">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="f0a9f-297">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-297">Value</span></span>                                                                        | <span data-ttu-id="f0a9f-298">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="f0a9f-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="f0a9f-300">Состояние работоспособности — нормальное.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0a9f-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-302">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-304">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f0a9f-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-309">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-310">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f0a9f-311">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-312">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-315">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-316">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-316">The label by which the object is known.</span></span> <span data-ttu-id="f0a9f-317">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "VMMS".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-318">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-319">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-321">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f0a9f-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f0a9f-322">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a9f-323">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f0a9f-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f0a9f-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f0a9f-343">)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a9f-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-345">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f0a9f-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-347">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-347">The current statuses of the object.</span></span> <span data-ttu-id="f0a9f-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-349">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-352">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="f0a9f-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="f0a9f-353">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f0a9f-354">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-355">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-358">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-359">Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="f0a9f-360">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-361">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-364">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-365">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="f0a9f-366">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="f0a9f-367">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-368">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-369">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-371">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-371">Provides high level status information.</span></span> <span data-ttu-id="f0a9f-372">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f0a9f-373">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a9f-374">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f0a9f-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-376"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f0a9f-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f0a9f-381">)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a9f-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-383">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-385">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="f0a9f-386">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f0a9f-387">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="f0a9f-388">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="f0a9f-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="f0a9f-389">В этом случае используется значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="f0a9f-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="f0a9f-390">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="f0a9f-391">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-391">Value</span></span>                                                                         | <span data-ttu-id="f0a9f-392">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="f0a9f-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f0a9f-394">Не применяется</span><span class="sxs-lookup"><span data-stu-id="f0a9f-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0a9f-395">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-396">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-398">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="f0a9f-399">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-403">Квалификаторы: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-404">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="f0a9f-405">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-406">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-407">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-409">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-410">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-411">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-413">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f0a9f-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f0a9f-414">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "служба работает нормально".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-415">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-416">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-418">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-419">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-419">The scoping system's creation class name.</span></span> <span data-ttu-id="f0a9f-420">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="f0a9f-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-422">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-424">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f0a9f-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-425">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="f0a9f-426">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-427">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-428">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-430">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f0a9f-431">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0a9f-432">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a9f-433">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0a9f-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a9f-435">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f0a9f-436">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0a9f-437">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0a9f-437">Remarks</span></span>

<span data-ttu-id="f0a9f-438">Доступ к классу **\_ виртуалсистемманажементсервице мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f0a9f-439">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a9f-440">Требования</span><span class="sxs-lookup"><span data-stu-id="f0a9f-440">Requirements</span></span>



| <span data-ttu-id="f0a9f-441">Требование</span><span class="sxs-lookup"><span data-stu-id="f0a9f-441">Requirement</span></span> | <span data-ttu-id="f0a9f-442">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a9f-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a9f-443">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0a9f-443">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a9f-444">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0a9f-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0a9f-445">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0a9f-445">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a9f-446">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0a9f-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0a9f-447">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0a9f-447">Namespace</span></span><br/>                | <span data-ttu-id="f0a9f-448">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f0a9f-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0a9f-449">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a9f-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a9f-450"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a9f-451">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a9f-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a9f-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0a9f-453">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0a9f-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a9f-454">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="f0a9f-455">[**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0a9f-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f0a9f-456">[**Мсвм \_ виртуалсистемманажементсервице (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0a9f-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f0a9f-457">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="f0a9f-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

