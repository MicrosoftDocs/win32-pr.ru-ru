---
description: Представляет параметры, используемые для проверки сетевого подключения виртуальной машины.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Класс Msvm_NetworkConnectionDiagnosticSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081498"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="62b74-103">\_Класс мсвм нетворкконнектиондиагностиксеттингдата</span><span class="sxs-lookup"><span data-stu-id="62b74-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="62b74-104">Представляет параметры, используемые для проверки сетевого подключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62b74-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="62b74-105">Используется методом [**диагносенетворкконнектион**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="62b74-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="62b74-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="62b74-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b74-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62b74-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="62b74-108">Члены</span><span class="sxs-lookup"><span data-stu-id="62b74-108">Members</span></span>

<span data-ttu-id="62b74-109">Класс **мсвм \_ нетворкконнектиондиагностиксеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62b74-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="62b74-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="62b74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62b74-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="62b74-111">Properties</span></span>

<span data-ttu-id="62b74-112">Класс **мсвм \_ нетворкконнектиондиагностиксеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62b74-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62b74-113">**исолатионид**</span><span class="sxs-lookup"><span data-stu-id="62b74-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62b74-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-116">Идентификатор изоляции.</span><span class="sxs-lookup"><span data-stu-id="62b74-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-117">**Отправители**</span><span class="sxs-lookup"><span data-stu-id="62b74-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62b74-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-120">Указывает, вызывается ли этот метод у отправителя или получателя.</span><span class="sxs-lookup"><span data-stu-id="62b74-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-121">**пайлоадсизе**</span><span class="sxs-lookup"><span data-stu-id="62b74-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62b74-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-124">Размер полезных данных.</span><span class="sxs-lookup"><span data-stu-id="62b74-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-125">**рецеиверип**</span><span class="sxs-lookup"><span data-stu-id="62b74-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62b74-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-128">IP-адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="62b74-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-129">**рецеивермак**</span><span class="sxs-lookup"><span data-stu-id="62b74-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62b74-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-132">MAC-адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="62b74-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-133">**сендерип**</span><span class="sxs-lookup"><span data-stu-id="62b74-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62b74-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-136">IP-адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="62b74-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62b74-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="62b74-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b74-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62b74-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62b74-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62b74-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62b74-140">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="62b74-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62b74-141">Требования</span><span class="sxs-lookup"><span data-stu-id="62b74-141">Requirements</span></span>



| <span data-ttu-id="62b74-142">Требование</span><span class="sxs-lookup"><span data-stu-id="62b74-142">Requirement</span></span> | <span data-ttu-id="62b74-143">Значение</span><span class="sxs-lookup"><span data-stu-id="62b74-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b74-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62b74-144">Minimum supported client</span></span><br/> | <span data-ttu-id="62b74-145">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="62b74-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62b74-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62b74-146">Minimum supported server</span></span><br/> | <span data-ttu-id="62b74-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="62b74-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="62b74-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62b74-148">Namespace</span></span><br/>                | <span data-ttu-id="62b74-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="62b74-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62b74-150">MOF</span><span class="sxs-lookup"><span data-stu-id="62b74-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62b74-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62b74-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62b74-152">DLL</span><span class="sxs-lookup"><span data-stu-id="62b74-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b74-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62b74-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62b74-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62b74-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b74-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="62b74-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




