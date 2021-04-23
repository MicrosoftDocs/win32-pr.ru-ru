---
description: Представляет параметры расширенного ACL порта.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Класс Msvm_EthernetSwitchPortExtendedAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663590"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="7aaf6-103">\_Класс мсвм есернетсвитчпортекстендедаклсеттингдата</span><span class="sxs-lookup"><span data-stu-id="7aaf6-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="7aaf6-104">Представляет параметры расширенного ACL порта.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="7aaf6-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aaf6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7aaf6-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="7aaf6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7aaf6-107">Members</span></span>

<span data-ttu-id="7aaf6-108">Класс **мсвм \_ есернетсвитчпортекстендедаклсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7aaf6-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7aaf6-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7aaf6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7aaf6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7aaf6-110">Properties</span></span>

<span data-ttu-id="7aaf6-111">Класс **мсвм \_ есернетсвитчпортекстендедаклсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7aaf6-112">**Действие**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-115">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-116">Действие расширенного ACL.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7aaf6-117">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="7aaf6-118">**Разрешить** (1)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="7aaf6-119">**Deny** (2)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7aaf6-120">**Направление**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-121">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-123">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-124">Указывает, применяется ли расширенный список ACL к входящему или исходящему направлению.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7aaf6-125">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="7aaf6-126">**Входящий** трафик (1)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="7aaf6-127">**Исходящие** (2)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7aaf6-128">**идлесессионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-131">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-132">Значение времени ожидания бездействующего сеанса (в секундах) для ACL с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-133">**исолатионид**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-136">Квалификаторы: **интерфацеверсион** (1), **интерфацеревисион** (0), **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-137">Идентификатор изоляции, к которому следует применить Расширенный список ACL.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-138">**локалипаддресс**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-141">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (4), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-142">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **вмидатаид** (6), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-147">Диапазон локальных портов.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-152">Понятное имя расширенного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-153">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-156">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **вмидатаид** (8), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-157">Строка протокола.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-158">**ремотеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-161">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (5), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-162">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-163">**ремотепорт**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **вмидатаид** (7), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-167">Диапазон удаленных портов.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-168">**С отслеживанием состояния**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-169">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-171">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-172">Указывает, является ли расширенный ACL без отслеживания состояния или без отслеживания состояния.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf6-173">**Weight**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aaf6-174">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aaf6-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aaf6-176">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aaf6-177">Вес, применяемый к расширенному списку ACL.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7aaf6-178">Требования</span><span class="sxs-lookup"><span data-stu-id="7aaf6-178">Requirements</span></span>



| <span data-ttu-id="7aaf6-179">Требование</span><span class="sxs-lookup"><span data-stu-id="7aaf6-179">Requirement</span></span> | <span data-ttu-id="7aaf6-180">Значение</span><span class="sxs-lookup"><span data-stu-id="7aaf6-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aaf6-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7aaf6-181">Minimum supported client</span></span><br/> | <span data-ttu-id="7aaf6-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7aaf6-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7aaf6-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7aaf6-183">Minimum supported server</span></span><br/> | <span data-ttu-id="7aaf6-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7aaf6-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7aaf6-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7aaf6-185">Namespace</span></span><br/>                | <span data-ttu-id="7aaf6-186">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7aaf6-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7aaf6-187">MOF</span><span class="sxs-lookup"><span data-stu-id="7aaf6-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aaf6-188"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf6-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7aaf6-189">DLL</span><span class="sxs-lookup"><span data-stu-id="7aaf6-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aaf6-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf6-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7aaf6-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7aaf6-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aaf6-192">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="7aaf6-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

