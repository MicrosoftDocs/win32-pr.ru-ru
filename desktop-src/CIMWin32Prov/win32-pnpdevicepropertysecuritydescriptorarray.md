---
description: Представляет свойство устройства PnP, состоящее из массива \_ элементов Win32 SecurityDescriptor.
ms.assetid: EDE24CDA-50C9-49C0-842E-C68891426AD6
ms.tgt_platform: multiple
title: Класс Win32_PnPDevicePropertySecurityDescriptorArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertySecurityDescriptorArray
- Win32_PnPDevicePropertySecurityDescriptorArray.Key
- Win32_PnPDevicePropertySecurityDescriptorArray.KeyName
- Win32_PnPDevicePropertySecurityDescriptorArray.Type
- Win32_PnPDevicePropertySecurityDescriptorArray.DeviceID
- Win32_PnPDevicePropertySecurityDescriptorArray.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 550290a19c275108d52472129084b80ef81b71e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990783"
---
# <a name="win32_pnpdevicepropertysecuritydescriptorarray-class"></a><span data-ttu-id="580ed-103">\_Класс Win32 пнпдевицепропертисекуритидескриптораррай</span><span class="sxs-lookup"><span data-stu-id="580ed-103">Win32\_PnPDevicePropertySecurityDescriptorArray class</span></span>

<span data-ttu-id="580ed-104">Представляет свойство устройства PnP, состоящее из массива элементов [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="580ed-104">Represents a PnP device property consisting of an array of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) elements.</span></span>

<span data-ttu-id="580ed-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="580ed-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="580ed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="580ed-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertySecurityDescriptorArray : Win32_PnPDeviceProperty
{
  string                   Key;
  string                   KeyName;
  Uint32                   Type;
  string                   DeviceID;
  Win32_SecurityDescriptor Data[];
};
```

## <a name="members"></a><span data-ttu-id="580ed-107">Члены</span><span class="sxs-lookup"><span data-stu-id="580ed-107">Members</span></span>

<span data-ttu-id="580ed-108">Класс **Win32 \_ пнпдевицепропертисекуритидескриптораррай** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="580ed-108">The **Win32\_PnPDevicePropertySecurityDescriptorArray** class has these types of members:</span></span>

-   [<span data-ttu-id="580ed-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="580ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="580ed-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="580ed-110">Properties</span></span>

<span data-ttu-id="580ed-111">Класс **Win32 \_ пнпдевицепропертисекуритидескриптораррай** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="580ed-111">The **Win32\_PnPDevicePropertySecurityDescriptorArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="580ed-112">**Data**</span><span class="sxs-lookup"><span data-stu-id="580ed-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="580ed-113">Тип данных: массив **[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**</span><span class="sxs-lookup"><span data-stu-id="580ed-113">Data type: **[**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)** array</span></span>
</dt> <dt>

<span data-ttu-id="580ed-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="580ed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="580ed-115">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="580ed-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="580ed-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="580ed-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="580ed-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="580ed-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="580ed-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="580ed-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="580ed-119">Определяет устройство PnP.</span><span class="sxs-lookup"><span data-stu-id="580ed-119">Identifies the PnP device.</span></span>

<span data-ttu-id="580ed-120">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="580ed-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="580ed-121">**Ключ**</span><span class="sxs-lookup"><span data-stu-id="580ed-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="580ed-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="580ed-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="580ed-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="580ed-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="580ed-124">Значение пары "ключ Name-Value", идентифицирующее свойство **данных** .</span><span class="sxs-lookup"><span data-stu-id="580ed-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="580ed-125">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="580ed-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="580ed-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="580ed-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="580ed-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="580ed-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="580ed-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="580ed-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="580ed-129">Имя пары ключей Name-Value, определяющее свойство **данных** .</span><span class="sxs-lookup"><span data-stu-id="580ed-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="580ed-130">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="580ed-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="580ed-131">**Тип**</span><span class="sxs-lookup"><span data-stu-id="580ed-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="580ed-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="580ed-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="580ed-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="580ed-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="580ed-134">Тип свойства **данных** .</span><span class="sxs-lookup"><span data-stu-id="580ed-134">The type of the **Data** property.</span></span>

<span data-ttu-id="580ed-135">Это свойство наследуется из [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="580ed-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="580ed-136">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="580ed-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="580ed-137">**Пусто** (0)</span><span class="sxs-lookup"><span data-stu-id="580ed-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="580ed-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="580ed-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="580ed-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="580ed-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="580ed-140">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="580ed-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="580ed-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="580ed-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="580ed-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="580ed-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="580ed-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="580ed-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="580ed-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="580ed-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="580ed-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="580ed-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="580ed-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="580ed-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="580ed-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="580ed-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="580ed-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="580ed-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="580ed-149">**Десятичное число** (12)</span><span class="sxs-lookup"><span data-stu-id="580ed-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="580ed-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="580ed-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="580ed-151">**Валюта** (14)</span><span class="sxs-lookup"><span data-stu-id="580ed-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="580ed-152">**Дата** (15)</span><span class="sxs-lookup"><span data-stu-id="580ed-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="580ed-153">**FileTime** (16)</span><span class="sxs-lookup"><span data-stu-id="580ed-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="580ed-154">**Логическое значение** (17)</span><span class="sxs-lookup"><span data-stu-id="580ed-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="580ed-155">**Строка** (18)</span><span class="sxs-lookup"><span data-stu-id="580ed-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="580ed-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="580ed-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="580ed-157">**Секуритидескрипторстринг** (20)</span><span class="sxs-lookup"><span data-stu-id="580ed-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="580ed-158">**Девпропкэй** (21)</span><span class="sxs-lookup"><span data-stu-id="580ed-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="580ed-159">**Девпроптипе** (22)</span><span class="sxs-lookup"><span data-stu-id="580ed-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="580ed-160">**Ошибка** (23)</span><span class="sxs-lookup"><span data-stu-id="580ed-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="580ed-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="580ed-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="580ed-162">**Стрингиндирект** (25)</span><span class="sxs-lookup"><span data-stu-id="580ed-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="580ed-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="580ed-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="580ed-164">26 — 4097</span><span class="sxs-lookup"><span data-stu-id="580ed-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="580ed-165">**Сбитеаррай** (4098)</span><span class="sxs-lookup"><span data-stu-id="580ed-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="580ed-166">**Двоичный** (4099)</span><span class="sxs-lookup"><span data-stu-id="580ed-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="580ed-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="580ed-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="580ed-168">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="580ed-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="580ed-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="580ed-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="580ed-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="580ed-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="580ed-171">**Флоатаррай** (4104)</span><span class="sxs-lookup"><span data-stu-id="580ed-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="580ed-172">**Даублеаррай** (4105)</span><span class="sxs-lookup"><span data-stu-id="580ed-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="580ed-173">**ДеЦималаррай** (4106)</span><span class="sxs-lookup"><span data-stu-id="580ed-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="580ed-174">**Гуидаррай** (4107)</span><span class="sxs-lookup"><span data-stu-id="580ed-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="580ed-175">**Курренциаррай** (4108)</span><span class="sxs-lookup"><span data-stu-id="580ed-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="580ed-176">**Датеаррай** (4109)</span><span class="sxs-lookup"><span data-stu-id="580ed-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="580ed-177">**Филетимеаррай** (4110)</span><span class="sxs-lookup"><span data-stu-id="580ed-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="580ed-178">**Булеанаррай** (4111)</span><span class="sxs-lookup"><span data-stu-id="580ed-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="580ed-179">**Стринглист** (4112)</span><span class="sxs-lookup"><span data-stu-id="580ed-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="580ed-180">**Секуритидескрипторлист** (4113)</span><span class="sxs-lookup"><span data-stu-id="580ed-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="580ed-181">**Секуритидескрипторстринглист** (8210)</span><span class="sxs-lookup"><span data-stu-id="580ed-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="580ed-182">**Девпропкэйаррай** (8211)</span><span class="sxs-lookup"><span data-stu-id="580ed-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="580ed-183">**Девпроптипеаррай** (8212)</span><span class="sxs-lookup"><span data-stu-id="580ed-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="580ed-184">**Еррораррай** (4117)</span><span class="sxs-lookup"><span data-stu-id="580ed-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="580ed-185">**Нтстатусаррай** (4118)</span><span class="sxs-lookup"><span data-stu-id="580ed-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="580ed-186">**Стрингиндиректлист** (4119)</span><span class="sxs-lookup"><span data-stu-id="580ed-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="580ed-187">**Неизвестно — проверьте девпропдеф. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="580ed-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="580ed-188">**Подлежит уточнению** (8217)</span><span class="sxs-lookup"><span data-stu-id="580ed-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="580ed-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="580ed-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="580ed-190">8218 — 4294967295</span><span class="sxs-lookup"><span data-stu-id="580ed-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="580ed-191">Требования</span><span class="sxs-lookup"><span data-stu-id="580ed-191">Requirements</span></span>



| <span data-ttu-id="580ed-192">Требование</span><span class="sxs-lookup"><span data-stu-id="580ed-192">Requirement</span></span> | <span data-ttu-id="580ed-193">Значение</span><span class="sxs-lookup"><span data-stu-id="580ed-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="580ed-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="580ed-194">Minimum supported client</span></span><br/> | <span data-ttu-id="580ed-195">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="580ed-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="580ed-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="580ed-196">Minimum supported server</span></span><br/> | <span data-ttu-id="580ed-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="580ed-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="580ed-198">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="580ed-198">Namespace</span></span><br/>                | <span data-ttu-id="580ed-199">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="580ed-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="580ed-200">MOF</span><span class="sxs-lookup"><span data-stu-id="580ed-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="580ed-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="580ed-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="580ed-202">DLL</span><span class="sxs-lookup"><span data-stu-id="580ed-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="580ed-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="580ed-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580ed-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="580ed-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580ed-205">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="580ed-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="580ed-206">**\_Пнпдевицепроперти Win32**</span><span class="sxs-lookup"><span data-stu-id="580ed-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="580ed-207">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="580ed-207">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="580ed-208">**жетдевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="580ed-208">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 
