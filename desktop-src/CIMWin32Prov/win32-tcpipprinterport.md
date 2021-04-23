---
description: '&Win32 \_ ткпиппринтерпорт \# 32; Класс WMI представляет точку доступа службы TCP/IP.'
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Класс Win32_TCPIPPrinterPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650461"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="67aba-103">\_Класс Win32 ткпиппринтерпорт</span><span class="sxs-lookup"><span data-stu-id="67aba-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="67aba-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ ткпиппринтерпорт для Win32** представляет точку доступа службы TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="67aba-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="67aba-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="67aba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="67aba-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="67aba-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67aba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67aba-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="67aba-108">Члены</span><span class="sxs-lookup"><span data-stu-id="67aba-108">Members</span></span>

<span data-ttu-id="67aba-109">Класс **Win32 \_ ткпиппринтерпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="67aba-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="67aba-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="67aba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67aba-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="67aba-111">Properties</span></span>

<span data-ttu-id="67aba-112">Класс **Win32 \_ ткпиппринтерпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67aba-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67aba-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="67aba-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67aba-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-116">Если **значение — true**, компьютер подсчитывает байты документа перед их отправкой на принтер, и принтер сообщает о количестве фактически считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="67aba-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="67aba-117">Эта возможность используется для диагностики при обнаружении недостающих байтов в выходных данных печати.</span><span class="sxs-lookup"><span data-stu-id="67aba-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="67aba-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-121">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="67aba-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="67aba-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67aba-122">A short textual description of the object.</span></span>

<span data-ttu-id="67aba-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67aba-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-127">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67aba-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67aba-128">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67aba-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="67aba-129">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="67aba-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="67aba-130">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67aba-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-134">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="67aba-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="67aba-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67aba-135">A textual description of the object.</span></span>

<span data-ttu-id="67aba-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-137">**хостаддресс**</span><span class="sxs-lookup"><span data-stu-id="67aba-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-140">Адрес устройства или сервера печати.</span><span class="sxs-lookup"><span data-stu-id="67aba-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67aba-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-142">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67aba-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-144">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="67aba-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="67aba-145">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="67aba-145">Indicates when the object was installed.</span></span> <span data-ttu-id="67aba-146">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="67aba-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="67aba-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="67aba-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-151">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67aba-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67aba-152">Уникально идентифицирует точку доступа службы и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="67aba-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="67aba-153">Эти функциональные возможности более подробно описаны в свойстве «описание» объекта.</span><span class="sxs-lookup"><span data-stu-id="67aba-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="67aba-154">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-155">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="67aba-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67aba-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-158">Число TCP-портов, используемых монитором портов для связи с устройством.</span><span class="sxs-lookup"><span data-stu-id="67aba-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-159">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="67aba-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67aba-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-162">Используемый протокол печати.</span><span class="sxs-lookup"><span data-stu-id="67aba-162">Printing protocol used.</span></span> <span data-ttu-id="67aba-163">Некоторые принтеры поддерживают только LPR.</span><span class="sxs-lookup"><span data-stu-id="67aba-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="67aba-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="67aba-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="67aba-165">RAW</span><span class="sxs-lookup"><span data-stu-id="67aba-165">RAW</span></span>

<span data-ttu-id="67aba-166">Непосредственная печать на устройстве или сервере печати.</span><span class="sxs-lookup"><span data-stu-id="67aba-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="67aba-167"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="67aba-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="67aba-168">LPR</span><span class="sxs-lookup"><span data-stu-id="67aba-168">LPR</span></span>

<span data-ttu-id="67aba-169">Устаревший протокол, который в конечном итоге заменяется на RAW.</span><span class="sxs-lookup"><span data-stu-id="67aba-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67aba-170">**Очередь**</span><span class="sxs-lookup"><span data-stu-id="67aba-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-173">Имя очереди печати на сервере при использовании с протоколом LPR.</span><span class="sxs-lookup"><span data-stu-id="67aba-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-174">**снмпкоммунити**</span><span class="sxs-lookup"><span data-stu-id="67aba-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-177">Значение уровня безопасности для устройства.</span><span class="sxs-lookup"><span data-stu-id="67aba-177">Security level value for the device.</span></span>

<span data-ttu-id="67aba-178">Пример: "Public"</span><span class="sxs-lookup"><span data-stu-id="67aba-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="67aba-179">**снмпдевиндекс**</span><span class="sxs-lookup"><span data-stu-id="67aba-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-180">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67aba-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-182">Номер индекса SNMP этого устройства для агента SNMP.</span><span class="sxs-lookup"><span data-stu-id="67aba-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-183">**снмпенаблед**</span><span class="sxs-lookup"><span data-stu-id="67aba-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67aba-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67aba-186">Если **значение — true**, этот принтер поддерживает стандарт [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (протокол сетевого управления) и может предоставлять подробные сведения о состоянии устройства.</span><span class="sxs-lookup"><span data-stu-id="67aba-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="67aba-187">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="67aba-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-190">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="67aba-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="67aba-191">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="67aba-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="67aba-192">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="67aba-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="67aba-193">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="67aba-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="67aba-194">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="67aba-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="67aba-195">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="67aba-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="67aba-196">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="67aba-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="67aba-197">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="67aba-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="67aba-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="67aba-199">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="67aba-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="67aba-200">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="67aba-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="67aba-201">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="67aba-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67aba-202">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="67aba-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67aba-203">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="67aba-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="67aba-204">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="67aba-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="67aba-205">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="67aba-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="67aba-206">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="67aba-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="67aba-207">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="67aba-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="67aba-208">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="67aba-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="67aba-209">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="67aba-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="67aba-210">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="67aba-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="67aba-211">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="67aba-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67aba-212">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="67aba-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-215">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67aba-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67aba-216">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="67aba-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="67aba-217">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="67aba-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67aba-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-221">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67aba-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67aba-222">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="67aba-222">The scoping system's name.</span></span>

<span data-ttu-id="67aba-223">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aba-224">**Тип**</span><span class="sxs-lookup"><span data-stu-id="67aba-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67aba-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67aba-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67aba-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67aba-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67aba-227">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67aba-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67aba-228">Тип SAP, например "подключено" или "перенаправлено".</span><span class="sxs-lookup"><span data-stu-id="67aba-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="67aba-229">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="67aba-230">**Запись** (1)</span><span class="sxs-lookup"><span data-stu-id="67aba-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="67aba-231">**Чтение** (2)</span><span class="sxs-lookup"><span data-stu-id="67aba-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="67aba-232">**Перенаправлено** (4)</span><span class="sxs-lookup"><span data-stu-id="67aba-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="67aba-233">**Команда NET \_ Подключено** (8)</span><span class="sxs-lookup"><span data-stu-id="67aba-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67aba-234">**неизвестно** (16)</span><span class="sxs-lookup"><span data-stu-id="67aba-234">**unknown** (16)</span></span>


<span data-ttu-id="67aba-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67aba-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="67aba-236">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67aba-236">Remarks</span></span>

<span data-ttu-id="67aba-237">Класс **Win32 \_ ткпиппринтерпорт** является производным от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md) , который является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="67aba-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="67aba-238">Для удаления экземпляра этого класса WMI требуется привилегия **селоаддриверпривилеже** .</span><span class="sxs-lookup"><span data-stu-id="67aba-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="67aba-239">В следующем фрагменте сценария показано, как создать соединение с WMI, которое использует эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="67aba-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="67aba-240">Примеры</span><span class="sxs-lookup"><span data-stu-id="67aba-240">Examples</span></span>

<span data-ttu-id="67aba-241">В следующем примере PowerShell удаляется принтер и связанный с ним порт принтера TCPIP.</span><span class="sxs-lookup"><span data-stu-id="67aba-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="67aba-242">Требования</span><span class="sxs-lookup"><span data-stu-id="67aba-242">Requirements</span></span>



| <span data-ttu-id="67aba-243">Требование</span><span class="sxs-lookup"><span data-stu-id="67aba-243">Requirement</span></span> | <span data-ttu-id="67aba-244">Значение</span><span class="sxs-lookup"><span data-stu-id="67aba-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67aba-245">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67aba-245">Minimum supported client</span></span><br/> | <span data-ttu-id="67aba-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67aba-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="67aba-247">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67aba-247">Minimum supported server</span></span><br/> | <span data-ttu-id="67aba-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67aba-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="67aba-249">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67aba-249">Namespace</span></span><br/>                | <span data-ttu-id="67aba-250">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67aba-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="67aba-251">MOF</span><span class="sxs-lookup"><span data-stu-id="67aba-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67aba-252"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67aba-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="67aba-253">DLL</span><span class="sxs-lookup"><span data-stu-id="67aba-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67aba-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67aba-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="67aba-255">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67aba-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67aba-256">**\_СЕРВИЦЕАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="67aba-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="67aba-257">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="67aba-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
