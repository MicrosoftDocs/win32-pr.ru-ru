---
description: Представляет конфигурацию коммутатора виртуальной Fibre Channel.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Класс Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540314"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="0f98c-103">\_Класс мсвм виртуалфксвитчсеттингдата</span><span class="sxs-lookup"><span data-stu-id="0f98c-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="0f98c-104">Представляет конфигурацию коммутатора виртуальной Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="0f98c-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="0f98c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0f98c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f98c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f98c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
};
```

## <a name="members"></a><span data-ttu-id="0f98c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0f98c-107">Members</span></span>

<span data-ttu-id="0f98c-108">Класс **мсвм \_ виртуалфксвитчсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f98c-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0f98c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f98c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f98c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f98c-110">Properties</span></span>

<span data-ttu-id="0f98c-111">Класс **мсвм \_ виртуалфксвитчсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f98c-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f98c-112">**аутоматикрековеряктион**</span><span class="sxs-lookup"><span data-stu-id="0f98c-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f98c-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-115">Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="0f98c-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="0f98c-116">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-117">**аутоматикшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="0f98c-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f98c-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-120">Действие, выполняемое для виртуальной машины при завершении работы узла.</span><span class="sxs-lookup"><span data-stu-id="0f98c-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="0f98c-121">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-122">**аутоматикстартупактион**</span><span class="sxs-lookup"><span data-stu-id="0f98c-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f98c-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-125">Действие, выполняемое для виртуальной машины при запуске узла.</span><span class="sxs-lookup"><span data-stu-id="0f98c-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="0f98c-126">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-127">**аутоматикстартупактионделай**</span><span class="sxs-lookup"><span data-stu-id="0f98c-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f98c-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-130">Время задержки перед автоматическим запуском виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="0f98c-131">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-132">**аутоматикстартупактионсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="0f98c-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f98c-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-135">Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы.</span><span class="sxs-lookup"><span data-stu-id="0f98c-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="0f98c-136">Меньшее значение указывает на более раннюю активацию.</span><span class="sxs-lookup"><span data-stu-id="0f98c-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="0f98c-137">Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="0f98c-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="0f98c-138">Значение 0 указывает, что последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="0f98c-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="0f98c-139">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-140">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0f98c-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-143">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0f98c-143">A short description of the object.</span></span> <span data-ttu-id="0f98c-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0f98c-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-145">**конфигуратиондатарут**</span><span class="sxs-lookup"><span data-stu-id="0f98c-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-148">Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="0f98c-149">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-150">**Файл ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="0f98c-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-153">Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="0f98c-154">Этот путь задается относительно свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="0f98c-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="0f98c-155">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="0f98c-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-159">Уникальный идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0f98c-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="0f98c-160">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0f98c-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f98c-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-164">Дата и время создания параметров.</span><span class="sxs-lookup"><span data-stu-id="0f98c-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="0f98c-165">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="0f98c-166">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-167">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f98c-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-170">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0f98c-170">A description of the object.</span></span> <span data-ttu-id="0f98c-171">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0f98c-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0f98c-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-175">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0f98c-175">A display name for the object.</span></span> <span data-ttu-id="0f98c-176">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0f98c-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-180">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0f98c-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-181">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="0f98c-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0f98c-182">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-183">**логдатарут**</span><span class="sxs-lookup"><span data-stu-id="0f98c-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-186">Путь к каталогу, в котором хранится информация журнала для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="0f98c-187">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-188">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="0f98c-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-189">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0f98c-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-191">Указанные пользователем примечания, связанные с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="0f98c-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="0f98c-192">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-193">**рековерифиле**</span><span class="sxs-lookup"><span data-stu-id="0f98c-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-196">Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="0f98c-197">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-198">**снапшотдатарут**</span><span class="sxs-lookup"><span data-stu-id="0f98c-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-201">Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="0f98c-202">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-203">**суспенддатарут**</span><span class="sxs-lookup"><span data-stu-id="0f98c-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-206">Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="0f98c-207">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-208">**свапфиледатарут**</span><span class="sxs-lookup"><span data-stu-id="0f98c-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-211">Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f98c-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="0f98c-212">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="0f98c-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-213">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="0f98c-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-216">Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра.</span><span class="sxs-lookup"><span data-stu-id="0f98c-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="0f98c-217">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f98c-218">**виртуалсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="0f98c-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f98c-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f98c-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f98c-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f98c-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f98c-221">Указывает тип виртуальной машины, которую представляют данные параметров.</span><span class="sxs-lookup"><span data-stu-id="0f98c-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="0f98c-222">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f98c-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f98c-223">Требования</span><span class="sxs-lookup"><span data-stu-id="0f98c-223">Requirements</span></span>



| <span data-ttu-id="0f98c-224">Требование</span><span class="sxs-lookup"><span data-stu-id="0f98c-224">Requirement</span></span> | <span data-ttu-id="0f98c-225">Значение</span><span class="sxs-lookup"><span data-stu-id="0f98c-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f98c-226">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f98c-226">Minimum supported client</span></span><br/> | <span data-ttu-id="0f98c-227">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0f98c-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f98c-228">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f98c-228">Minimum supported server</span></span><br/> | <span data-ttu-id="0f98c-229">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0f98c-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f98c-230">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f98c-230">Namespace</span></span><br/>                | <span data-ttu-id="0f98c-231">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0f98c-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f98c-232">MOF</span><span class="sxs-lookup"><span data-stu-id="0f98c-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f98c-233"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f98c-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f98c-234">DLL</span><span class="sxs-lookup"><span data-stu-id="0f98c-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f98c-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f98c-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

