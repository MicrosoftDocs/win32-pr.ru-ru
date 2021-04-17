---
description: Представляет параметры разгрузки коммутатора.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Класс Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684704"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="0297b-103">\_Класс мсвм есернетсвитчхардвареоффлоадсеттингдата</span><span class="sxs-lookup"><span data-stu-id="0297b-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="0297b-104">Представляет параметры разгрузки коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0297b-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="0297b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0297b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0297b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0297b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="0297b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0297b-107">Members</span></span>

<span data-ttu-id="0297b-108">Класс **мсвм \_ есернетсвитчхардвареоффлоадсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0297b-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0297b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0297b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0297b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0297b-110">Properties</span></span>

<span data-ttu-id="0297b-111">Класс **мсвм \_ есернетсвитчхардвареоффлоадсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0297b-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0297b-112">**дефаулткуеуевммкенаблед**</span><span class="sxs-lookup"><span data-stu-id="0297b-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0297b-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0297b-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0297b-115">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-116">Задает параметры ВММК для очереди по умолчанию vSwitch.</span><span class="sxs-lookup"><span data-stu-id="0297b-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="0297b-117">**дефаулткуеуевммккуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="0297b-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0297b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0297b-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0297b-120">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-121">Указывает количество очередей для очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0297b-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="0297b-122">**дефаулткуеуеврссенаблед**</span><span class="sxs-lookup"><span data-stu-id="0297b-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0297b-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0297b-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0297b-125">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-126">Задает параметры VRss для очереди по умолчанию в vSwitch.</span><span class="sxs-lookup"><span data-stu-id="0297b-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="0297b-127">**дефаулткуеуеврссексклудепримарипроцессор**</span><span class="sxs-lookup"><span data-stu-id="0297b-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0297b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0297b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0297b-130">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-131">Указывает, исключается ли основной ЦП VMQ из таблицы косвенных обращений VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="0297b-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="0297b-132">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="0297b-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0297b-133">**дефаулткуеуеврссиндепенденсостспреадинг**</span><span class="sxs-lookup"><span data-stu-id="0297b-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0297b-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0297b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0297b-136">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-137">Указывает, следует ли всегда выполнять распространение VRSS для очереди по умолчанию независимо от состояния RSS внешней впорт.</span><span class="sxs-lookup"><span data-stu-id="0297b-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="0297b-138">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="0297b-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0297b-139">**дефаулткуеуеврссминкуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="0297b-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0297b-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0297b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0297b-142">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-143">Указывает минимальное число очередей, используемых для VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="0297b-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="0297b-144">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="0297b-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0297b-145">**дефаулткуеуеврсскуеуесчедулингмоде**</span><span class="sxs-lookup"><span data-stu-id="0297b-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0297b-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0297b-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0297b-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0297b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0297b-148">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="0297b-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0297b-149">Указывает, каким способом очереди VRSS/ВММК связаны с разными процессорами узла.</span><span class="sxs-lookup"><span data-stu-id="0297b-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="0297b-150">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="0297b-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0297b-151">Требования</span><span class="sxs-lookup"><span data-stu-id="0297b-151">Requirements</span></span>



| <span data-ttu-id="0297b-152">Требование</span><span class="sxs-lookup"><span data-stu-id="0297b-152">Requirement</span></span> | <span data-ttu-id="0297b-153">Значение</span><span class="sxs-lookup"><span data-stu-id="0297b-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0297b-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0297b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="0297b-155">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="0297b-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0297b-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0297b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="0297b-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0297b-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0297b-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0297b-158">Namespace</span></span><br/>                | <span data-ttu-id="0297b-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0297b-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0297b-160">MOF</span><span class="sxs-lookup"><span data-stu-id="0297b-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0297b-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0297b-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0297b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="0297b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0297b-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0297b-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0297b-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0297b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0297b-165">**Мсвм \_ есернетсвитчфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="0297b-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




