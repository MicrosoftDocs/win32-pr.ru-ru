---
description: Представляет текущую конфигурацию виртуального коммутатора Ethernet.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Класс Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683166"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="d9a1a-103">\_Класс мсвм виртуалесернетсвитчсеттингдата</span><span class="sxs-lookup"><span data-stu-id="d9a1a-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="d9a1a-104">Представляет текущую конфигурацию виртуального коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="d9a1a-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a1a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9a1a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="d9a1a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d9a1a-107">Members</span></span>

<span data-ttu-id="d9a1a-108">Класс **мсвм \_ виртуалесернетсвитчсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9a1a-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d9a1a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9a1a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9a1a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9a1a-110">Properties</span></span>

<span data-ttu-id="d9a1a-111">Класс **мсвм \_ виртуалесернетсвитчсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9a1a-112">**ассоЦиатедресаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-115">Список пулов ресурсов узлов, которые будут связаны или которые в настоящее время связаны с коммутатором Ethernet, для распределения Ethernet-подключений между виртуальной машиной и коммутатором Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="d9a1a-116">Каждое значение должно соответствовать рабочему URI производства \_ \_ унтипединстанцепас, как определено в DSP0207.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="d9a1a-117">Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-118">**аутоматикрековеряктион**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-121">Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="d9a1a-122">Сбои в этом случае означают сбой, который обнаруживается платформой размещения, например условие состояния ожидания без взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="d9a1a-123">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-124">**аутоматикшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-127">Действие, выполняемое для виртуальной машины при завершении работы узла.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="d9a1a-128">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-129">**аутоматикстартупактион**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-132">Действие, выполняемое для виртуальной машины при запуске узла.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="d9a1a-133">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-134">**аутоматикстартупактионделай**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-137">Время задержки перед автоматическим запуском виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="d9a1a-138">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-139">**аутоматикстартупактионсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-142">Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="d9a1a-143">Меньшее значение указывает на более раннюю активацию.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="d9a1a-144">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-145">**бандвидсресерватионмоде**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a1a-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-148">Режим резервирования пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d9a1a-149">**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="d9a1a-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="d9a1a-150">**Вес** (1)</span><span class="sxs-lookup"><span data-stu-id="d9a1a-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="d9a1a-151">**Absolute** (2)</span><span class="sxs-lookup"><span data-stu-id="d9a1a-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d9a1a-152">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="d9a1a-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9a1a-153">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-156">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-156">A short description of the object.</span></span> <span data-ttu-id="d9a1a-157">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры виртуального коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d9a1a-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-158">**конфигуратиондатарут**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-161">Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="d9a1a-162">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-163">**Файл ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-166">Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="d9a1a-167">Этот путь задается относительно свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="d9a1a-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="d9a1a-168">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-172">Уникальный идентификатор конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="d9a1a-173">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-175">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-177">Дата и время создания параметров.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="d9a1a-178">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9a1a-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-179">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-182">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-182">A description of the object.</span></span> <span data-ttu-id="d9a1a-183">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "активные параметры для виртуального коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d9a1a-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-187">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-187">A display name for the object.</span></span> <span data-ttu-id="d9a1a-188">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9a1a-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-189">**екстенсионордер**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-190">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a1a-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-192">Массив внедренных экземпляров класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющих расширения коммутаторов, привязанные к этому коммутатору, в том порядке, в котором они применяются.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-196">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-197">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d9a1a-198">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".</span><span class="sxs-lookup"><span data-stu-id="d9a1a-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-199">**иовпреферред**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-200">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a1a-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-202">Указывает, является ли однокорневой сервер ввода/вывода (SR-IOV) предпочтительнее, если это возможно, на базовом адаптере.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-203">**логдатарут**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-206">Путь к каталогу, в котором хранится информация журнала для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="d9a1a-207">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-208">**макснуммакаддресс**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-209">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-211">Указывает максимальное число уникальных MAC-адресов, которые могут быть получены коммутатором для поддержки обучения MAC-адресов, как определено в стандарте IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="d9a1a-212">Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-213">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-214">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-216">Указанные пользователем примечания, связанные с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="d9a1a-217">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9a1a-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-218">**паккетдиректенаблед**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a1a-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-221">Указывает, следует ли использовать PacketDirect, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="d9a1a-222">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="d9a1a-223">Это свойство было добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d9a1a-224">**рековерифиле**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-227">Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="d9a1a-228">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-229">**снапшотдатарут**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-232">Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="d9a1a-233">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-234">**суспенддатарут**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-237">Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="d9a1a-238">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-239">**свапфиледатарут**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-242">Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="d9a1a-243">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-244">**теаминженаблед**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-246">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a1a-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-247">Указывает, следует ли использовать объединение сетевых карт.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="d9a1a-248">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="d9a1a-249">Это свойство было добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d9a1a-250">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-253">Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="d9a1a-254">Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9a1a-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-255">**виртуалсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-258">Указывает тип виртуальной машины, которую представляют данные параметров.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="d9a1a-259">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9a1a-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9a1a-260">**вланконнектион**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a1a-261">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d9a1a-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9a1a-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a1a-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9a1a-263">Список идентификаторов VLAN, к которым может получить доступ этот коммутатор.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="d9a1a-264">Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9a1a-265">Требования</span><span class="sxs-lookup"><span data-stu-id="d9a1a-265">Requirements</span></span>



| <span data-ttu-id="d9a1a-266">Требование</span><span class="sxs-lookup"><span data-stu-id="d9a1a-266">Requirement</span></span> | <span data-ttu-id="d9a1a-267">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a1a-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a1a-268">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9a1a-268">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a1a-269">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d9a1a-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d9a1a-270">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9a1a-270">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a1a-271">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d9a1a-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9a1a-272">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9a1a-272">Namespace</span></span><br/>                | <span data-ttu-id="d9a1a-273">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d9a1a-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d9a1a-274">MOF</span><span class="sxs-lookup"><span data-stu-id="d9a1a-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9a1a-275"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9a1a-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9a1a-276">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a1a-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a1a-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9a1a-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

