---
title: Класс MDM_DeviceStatus_CellularIdentities01_01
description: Класс MDM \_ девицестатус \_ CellularIdentities01 \_ 01 позволяет запрашивать, соответствует ли устройство политике шифрования предприятия.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- Класс MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892317"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="9a21b-105">\_Класс MDM девицестатус \_ CellularIdentities01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="9a21b-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="9a21b-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9a21b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9a21b-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9a21b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9a21b-108">Класс **MDM \_ девицестатус \_ CellularIdentities01 \_ 01** позволяет запрашивать, соответствует ли устройство политике шифрования предприятия.</span><span class="sxs-lookup"><span data-stu-id="9a21b-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="9a21b-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9a21b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a21b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a21b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="9a21b-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9a21b-111">Members</span></span>

<span data-ttu-id="9a21b-112">Класс **MDM \_ девицестатус \_ CellularIdentities01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9a21b-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="9a21b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a21b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a21b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a21b-114">Properties</span></span>

<span data-ttu-id="9a21b-115">Класс **MDM \_ девицестатус \_ CellularIdentities01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="9a21b-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9a21b-116">коммерЦиализатионоператор</span><span class="sxs-lookup"><span data-stu-id="9a21b-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9a21b-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="9a21b-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9a21b-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="9a21b-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9a21b-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9a21b-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a21b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a21b-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9a21b-129">Узел для запросов к SIM-картам.</span><span class="sxs-lookup"><span data-stu-id="9a21b-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="9a21b-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9a21b-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a21b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a21b-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9a21b-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9a21b-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="9a21b-135">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="9a21b-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="9a21b-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9a21b-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a21b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9a21b-139">роамингкомплианце</span><span class="sxs-lookup"><span data-stu-id="9a21b-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a21b-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9a21b-142">роамингстатус</span><span class="sxs-lookup"><span data-stu-id="9a21b-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a21b-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a21b-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a21b-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a21b-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a21b-145">Требования</span><span class="sxs-lookup"><span data-stu-id="9a21b-145">Requirements</span></span>



| <span data-ttu-id="9a21b-146">Требование</span><span class="sxs-lookup"><span data-stu-id="9a21b-146">Requirement</span></span> | <span data-ttu-id="9a21b-147">Значение</span><span class="sxs-lookup"><span data-stu-id="9a21b-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a21b-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a21b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9a21b-149">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9a21b-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a21b-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a21b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9a21b-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9a21b-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9a21b-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a21b-152">Namespace</span></span><br/>                | <span data-ttu-id="9a21b-153">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9a21b-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9a21b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9a21b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a21b-155"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a21b-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a21b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9a21b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a21b-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a21b-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a21b-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a21b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a21b-159">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9a21b-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

