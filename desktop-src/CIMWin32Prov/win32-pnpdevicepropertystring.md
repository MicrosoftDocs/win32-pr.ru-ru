---
description: Представляет свойство устройства PnP типа String.
ms.assetid: 10D5C2B1-E5B4-4A7E-BC5E-5F6A4ABDDBF7
ms.tgt_platform: multiple
title: Класс Win32_PnPDevicePropertyString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertyString
- Win32_PnPDevicePropertyString.Key
- Win32_PnPDevicePropertyString.KeyName
- Win32_PnPDevicePropertyString.Type
- Win32_PnPDevicePropertyString.DeviceID
- Win32_PnPDevicePropertyString.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea9b0c0b9248af16f8bc0b629332429f54f46563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896466"
---
# <a name="win32_pnpdevicepropertystring-class"></a><span data-ttu-id="72632-103">\_Класс Win32 пнпдевицепропертистринг</span><span class="sxs-lookup"><span data-stu-id="72632-103">Win32\_PnPDevicePropertyString class</span></span>

<span data-ttu-id="72632-104">Представляет свойство устройства PnP типа **String**.</span><span class="sxs-lookup"><span data-stu-id="72632-104">Represents a PnP device property of type **string**.</span></span>

<span data-ttu-id="72632-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="72632-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72632-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72632-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertyString : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="72632-107">Члены</span><span class="sxs-lookup"><span data-stu-id="72632-107">Members</span></span>

<span data-ttu-id="72632-108">Класс **Win32 \_ пнпдевицепропертистринг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72632-108">The **Win32\_PnPDevicePropertyString** class has these types of members:</span></span>

-   [<span data-ttu-id="72632-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="72632-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72632-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="72632-110">Properties</span></span>

<span data-ttu-id="72632-111">Класс **Win32 \_ пнпдевицепропертистринг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="72632-111">The **Win32\_PnPDevicePropertyString** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72632-112">**Data**</span><span class="sxs-lookup"><span data-stu-id="72632-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72632-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72632-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72632-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72632-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72632-115">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="72632-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="72632-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="72632-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72632-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72632-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72632-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72632-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72632-119">Определяет устройство PnP.</span><span class="sxs-lookup"><span data-stu-id="72632-119">Identifies the PnP device.</span></span>

<span data-ttu-id="72632-120">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="72632-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="72632-121">**Ключ**</span><span class="sxs-lookup"><span data-stu-id="72632-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72632-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72632-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72632-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72632-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72632-124">Значение пары "ключ Name-Value", идентифицирующее свойство **данных** .</span><span class="sxs-lookup"><span data-stu-id="72632-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="72632-125">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="72632-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="72632-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="72632-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72632-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72632-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72632-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72632-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72632-129">Имя пары ключей Name-Value, определяющее свойство **данных** .</span><span class="sxs-lookup"><span data-stu-id="72632-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="72632-130">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="72632-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="72632-131">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72632-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72632-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72632-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72632-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72632-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72632-134">Тип свойства **данных** .</span><span class="sxs-lookup"><span data-stu-id="72632-134">The type of the **Data** property.</span></span>

<span data-ttu-id="72632-135">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="72632-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="72632-136">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="72632-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="72632-137">**Пусто** (0)</span><span class="sxs-lookup"><span data-stu-id="72632-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="72632-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="72632-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="72632-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="72632-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="72632-140">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="72632-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="72632-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="72632-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="72632-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="72632-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="72632-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="72632-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="72632-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="72632-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="72632-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="72632-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="72632-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="72632-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="72632-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="72632-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="72632-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="72632-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="72632-149">**Десятичное число** (12)</span><span class="sxs-lookup"><span data-stu-id="72632-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="72632-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="72632-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="72632-151">**Валюта** (14)</span><span class="sxs-lookup"><span data-stu-id="72632-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="72632-152">**Дата** (15)</span><span class="sxs-lookup"><span data-stu-id="72632-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="72632-153">**FileTime** (16)</span><span class="sxs-lookup"><span data-stu-id="72632-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="72632-154">**Логическое значение** (17)</span><span class="sxs-lookup"><span data-stu-id="72632-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="72632-155">**Строка** (18)</span><span class="sxs-lookup"><span data-stu-id="72632-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="72632-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="72632-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="72632-157">**Секуритидескрипторстринг** (20)</span><span class="sxs-lookup"><span data-stu-id="72632-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="72632-158">**Девпропкэй** (21)</span><span class="sxs-lookup"><span data-stu-id="72632-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="72632-159">**Девпроптипе** (22)</span><span class="sxs-lookup"><span data-stu-id="72632-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="72632-160">**Ошибка** (23)</span><span class="sxs-lookup"><span data-stu-id="72632-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="72632-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="72632-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="72632-162">**Стрингиндирект** (25)</span><span class="sxs-lookup"><span data-stu-id="72632-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="72632-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="72632-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="72632-164">26 — 4097</span><span class="sxs-lookup"><span data-stu-id="72632-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="72632-165">**Сбитеаррай** (4098)</span><span class="sxs-lookup"><span data-stu-id="72632-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="72632-166">**Двоичный** (4099)</span><span class="sxs-lookup"><span data-stu-id="72632-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="72632-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="72632-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="72632-168">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="72632-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="72632-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="72632-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="72632-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="72632-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="72632-171">**Флоатаррай** (4104)</span><span class="sxs-lookup"><span data-stu-id="72632-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="72632-172">**Даублеаррай** (4105)</span><span class="sxs-lookup"><span data-stu-id="72632-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="72632-173">**ДеЦималаррай** (4106)</span><span class="sxs-lookup"><span data-stu-id="72632-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="72632-174">**Гуидаррай** (4107)</span><span class="sxs-lookup"><span data-stu-id="72632-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="72632-175">**Курренциаррай** (4108)</span><span class="sxs-lookup"><span data-stu-id="72632-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="72632-176">**Датеаррай** (4109)</span><span class="sxs-lookup"><span data-stu-id="72632-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="72632-177">**Филетимеаррай** (4110)</span><span class="sxs-lookup"><span data-stu-id="72632-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="72632-178">**Булеанаррай** (4111)</span><span class="sxs-lookup"><span data-stu-id="72632-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="72632-179">**Стринглист** (4112)</span><span class="sxs-lookup"><span data-stu-id="72632-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="72632-180">**Секуритидескрипторлист** (4113)</span><span class="sxs-lookup"><span data-stu-id="72632-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="72632-181">**Секуритидескрипторстринглист** (8210)</span><span class="sxs-lookup"><span data-stu-id="72632-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="72632-182">**Девпропкэйаррай** (8211)</span><span class="sxs-lookup"><span data-stu-id="72632-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="72632-183">**Девпроптипеаррай** (8212)</span><span class="sxs-lookup"><span data-stu-id="72632-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="72632-184">**Еррораррай** (4117)</span><span class="sxs-lookup"><span data-stu-id="72632-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="72632-185">**Нтстатусаррай** (4118)</span><span class="sxs-lookup"><span data-stu-id="72632-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="72632-186">**Стрингиндиректлист** (4119)</span><span class="sxs-lookup"><span data-stu-id="72632-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="72632-187">**Неизвестно — проверьте девпропдеф. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="72632-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="72632-188">**Подлежит уточнению** (8217)</span><span class="sxs-lookup"><span data-stu-id="72632-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="72632-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="72632-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="72632-190">8218 — 4294967295</span><span class="sxs-lookup"><span data-stu-id="72632-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72632-191">Требования</span><span class="sxs-lookup"><span data-stu-id="72632-191">Requirements</span></span>



| <span data-ttu-id="72632-192">Требование</span><span class="sxs-lookup"><span data-stu-id="72632-192">Requirement</span></span> | <span data-ttu-id="72632-193">Значение</span><span class="sxs-lookup"><span data-stu-id="72632-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72632-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72632-194">Minimum supported client</span></span><br/> | <span data-ttu-id="72632-195">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="72632-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72632-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72632-196">Minimum supported server</span></span><br/> | <span data-ttu-id="72632-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="72632-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="72632-198">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72632-198">Namespace</span></span><br/>                | <span data-ttu-id="72632-199">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="72632-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72632-200">MOF</span><span class="sxs-lookup"><span data-stu-id="72632-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72632-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72632-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72632-202">DLL</span><span class="sxs-lookup"><span data-stu-id="72632-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72632-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72632-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72632-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72632-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72632-205">**\_Пнпдевицепроперти Win32**</span><span class="sxs-lookup"><span data-stu-id="72632-205">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> </dl>

 

 




