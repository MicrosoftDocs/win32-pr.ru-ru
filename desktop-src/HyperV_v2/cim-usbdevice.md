---
description: Характеристики управления USB-устройства.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: Класс CIM_USBDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683253"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="70197-103">Класс CIM_USBDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="70197-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="70197-104">Характеристики управления USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="70197-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70197-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="70197-106">Члены</span><span class="sxs-lookup"><span data-stu-id="70197-106">Members</span></span>

<span data-ttu-id="70197-107">Класс **CIM \_ усбдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70197-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="70197-108">Методы</span><span class="sxs-lookup"><span data-stu-id="70197-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="70197-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="70197-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70197-110">Методы</span><span class="sxs-lookup"><span data-stu-id="70197-110">Methods</span></span>

<span data-ttu-id="70197-111">Класс **CIM \_ усбдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="70197-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="70197-112">Метод</span><span class="sxs-lookup"><span data-stu-id="70197-112">Method</span></span>                                               | <span data-ttu-id="70197-113">Описание</span><span class="sxs-lookup"><span data-stu-id="70197-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="70197-114">**Двухбайтовый**</span><span class="sxs-lookup"><span data-stu-id="70197-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="70197-115">Извлекает дескриптор USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="70197-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="70197-116">Properties</span></span>

<span data-ttu-id="70197-117">Класс **CIM \_ усбдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70197-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70197-118">**класскоде**</span><span class="sxs-lookup"><span data-stu-id="70197-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-121">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бдевицекласс")</span><span class="sxs-lookup"><span data-stu-id="70197-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="70197-122">Код класса USB.</span><span class="sxs-lookup"><span data-stu-id="70197-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="70197-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="70197-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-124">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70197-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70197-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70197-126">Интервал времени ожидания, настраиваемый приложениями управления, поддерживающими перенаправление USB.</span><span class="sxs-lookup"><span data-stu-id="70197-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="70197-127">Когда служба перенаправления перенаправляет команду USB-устройства на удаленное устройство, а удаленное устройство не ответит до истечения времени ожидания, служба перенаправления будет эмулировать событие извлечения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="70197-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="70197-128">Кроме того, служба может повторно выполнить команду или попытаться восстановить подключение к удаленному устройству.</span><span class="sxs-lookup"><span data-stu-id="70197-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-129">**курренталтернатесеттингс**</span><span class="sxs-lookup"><span data-stu-id="70197-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-130">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="70197-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-132">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ усбдевице**.**Куррентконфигвалуе**")</span><span class="sxs-lookup"><span data-stu-id="70197-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="70197-133">Массив, содержащий альтернативные параметры для каждого интерфейса в текущей конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-134">**куррентконфигвалуе**</span><span class="sxs-lookup"><span data-stu-id="70197-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-135">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-137">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ усбдевице**.**Курренталтернатесеттингс**")</span><span class="sxs-lookup"><span data-stu-id="70197-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="70197-138">Конфигурация, выбранная в настоящее время для устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="70197-139">Если это значение равно нулю, устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="70197-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="70197-140">**девицерелеасенумбер**</span><span class="sxs-lookup"><span data-stu-id="70197-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70197-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70197-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бкддевице")</span><span class="sxs-lookup"><span data-stu-id="70197-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="70197-144">Номер выпуска устройства в формате BCD.</span><span class="sxs-lookup"><span data-stu-id="70197-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="70197-145">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="70197-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70197-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70197-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| имануфактурер")</span><span class="sxs-lookup"><span data-stu-id="70197-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="70197-149">Строка изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="70197-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-151">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-153">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бмакспаккетсизе")</span><span class="sxs-lookup"><span data-stu-id="70197-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="70197-154">Максимальный размер пакета для конечной точки USB 0.</span><span class="sxs-lookup"><span data-stu-id="70197-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="70197-155">**нумберофконфигс**</span><span class="sxs-lookup"><span data-stu-id="70197-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-156">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-158">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бнумконфигуратионс")</span><span class="sxs-lookup"><span data-stu-id="70197-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="70197-159">Количество конфигураций устройств, определенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-160">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="70197-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70197-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70197-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-163">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| ипродукт")</span><span class="sxs-lookup"><span data-stu-id="70197-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="70197-164">Строка продукта устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-165">**Кодом**</span><span class="sxs-lookup"><span data-stu-id="70197-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70197-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70197-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-168">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| идпродукт")</span><span class="sxs-lookup"><span data-stu-id="70197-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="70197-169">Идентификатор продукта, назначенный устройству изготовителем.</span><span class="sxs-lookup"><span data-stu-id="70197-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="70197-170">**протоколкоде**</span><span class="sxs-lookup"><span data-stu-id="70197-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-171">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-173">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бдевицепротокол")</span><span class="sxs-lookup"><span data-stu-id="70197-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="70197-174">Код протокола USB.</span><span class="sxs-lookup"><span data-stu-id="70197-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="70197-175">**Номер**</span><span class="sxs-lookup"><span data-stu-id="70197-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70197-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70197-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-178">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| исериалнумбер")</span><span class="sxs-lookup"><span data-stu-id="70197-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="70197-179">Серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="70197-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="70197-180">**субкласскоде**</span><span class="sxs-lookup"><span data-stu-id="70197-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-181">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="70197-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70197-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-183">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бдевицесубкласс")</span><span class="sxs-lookup"><span data-stu-id="70197-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="70197-184">Код подкласса USB.</span><span class="sxs-lookup"><span data-stu-id="70197-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="70197-185">**усбверсион**</span><span class="sxs-lookup"><span data-stu-id="70197-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-186">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70197-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70197-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70197-188">Последняя версия USB, поддерживаемая USB-устройством.</span><span class="sxs-lookup"><span data-stu-id="70197-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="70197-189">Свойство выражается в виде двоичного десятичного числа (BCD), содержащего десятичную запятую между 2-и третьими цифрами.</span><span class="sxs-lookup"><span data-stu-id="70197-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="70197-190">Например, значение 0x201 указывает, что поддерживается версия 2,01.</span><span class="sxs-lookup"><span data-stu-id="70197-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="70197-191">**усбверсионинбкд**</span><span class="sxs-lookup"><span data-stu-id="70197-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70197-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70197-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-194">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| бкдусб")</span><span class="sxs-lookup"><span data-stu-id="70197-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="70197-195">Номер спецификации USB, который соответствует устройству.</span><span class="sxs-lookup"><span data-stu-id="70197-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="70197-196">Это свойство форматируется с использованием формата BCD.</span><span class="sxs-lookup"><span data-stu-id="70197-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="70197-197">**Поставщика**</span><span class="sxs-lookup"><span data-stu-id="70197-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70197-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70197-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70197-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70197-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70197-200">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Спецификация универсальной последовательной шины. USB — при \| стандартном дескрипторе устройства \| идвендор")</span><span class="sxs-lookup"><span data-stu-id="70197-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="70197-201">Идентификатор поставщика, назначенный устройству по USB.org.</span><span class="sxs-lookup"><span data-stu-id="70197-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70197-202">Требования</span><span class="sxs-lookup"><span data-stu-id="70197-202">Requirements</span></span>



| <span data-ttu-id="70197-203">Требование</span><span class="sxs-lookup"><span data-stu-id="70197-203">Requirement</span></span> | <span data-ttu-id="70197-204">Значение</span><span class="sxs-lookup"><span data-stu-id="70197-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70197-205">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70197-205">Minimum supported client</span></span><br/> | <span data-ttu-id="70197-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="70197-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="70197-207">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70197-207">Minimum supported server</span></span><br/> | <span data-ttu-id="70197-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="70197-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="70197-209">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70197-209">Namespace</span></span><br/>                | <span data-ttu-id="70197-210">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="70197-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="70197-211">MOF</span><span class="sxs-lookup"><span data-stu-id="70197-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70197-212"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70197-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70197-213">DLL</span><span class="sxs-lookup"><span data-stu-id="70197-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70197-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70197-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70197-215">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70197-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70197-216">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="70197-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

