---
description: Представляет идентифицирующие сведения о видеомониторе, например название производителя, год изготовления или серийный номер.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Класс Вмимониторид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714069"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="e89ed-103">Класс Вмимониторид</span><span class="sxs-lookup"><span data-stu-id="e89ed-103">WmiMonitorID class</span></span>

<span data-ttu-id="e89ed-104">Класс WMI **вмимониторид** представляет идентифицирующие сведения о видеомониторе, например название производителя, год изготовления или серийный номер.</span><span class="sxs-lookup"><span data-stu-id="e89ed-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="e89ed-105">Данные в этом классе соответствуют данным в блоке идентификации поставщика или продукта определение входного видео для расширенного расширенного представления идентификационных данных (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="e89ed-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89ed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e89ed-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="e89ed-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e89ed-107">Members</span></span>

<span data-ttu-id="e89ed-108">Класс **вмимониторид** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e89ed-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="e89ed-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e89ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e89ed-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e89ed-110">Properties</span></span>

<span data-ttu-id="e89ed-111">Класс **вмимониторид** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e89ed-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e89ed-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="e89ed-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e89ed-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="e89ed-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e89ed-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e89ed-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-119">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e89ed-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-120">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="e89ed-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="e89ed-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-122">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e89ed-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-124">Имя производителя.</span><span class="sxs-lookup"><span data-stu-id="e89ed-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-125">**мануфактурернамеленгс**</span><span class="sxs-lookup"><span data-stu-id="e89ed-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e89ed-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-128">Длина имени производителя, расположенного в свойстве **ManufacturerName** .</span><span class="sxs-lookup"><span data-stu-id="e89ed-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-129">**продукткодеид**</span><span class="sxs-lookup"><span data-stu-id="e89ed-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-130">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e89ed-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-132">Код продукта, назначенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e89ed-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-133">**сериалнумберид**</span><span class="sxs-lookup"><span data-stu-id="e89ed-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e89ed-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-136">Серийный номер.</span><span class="sxs-lookup"><span data-stu-id="e89ed-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e89ed-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-138">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e89ed-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-140">Понятное имя монитора.</span><span class="sxs-lookup"><span data-stu-id="e89ed-140">The friendly name of the monitor.</span></span> <span data-ttu-id="e89ed-141">Размер имени — это длина, заданная свойством Усерфриендлинамеленгс.</span><span class="sxs-lookup"><span data-stu-id="e89ed-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-142">усерфриендлинамеленгс</span><span class="sxs-lookup"><span data-stu-id="e89ed-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e89ed-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-145">Число символов в имени, расположенном в свойстве Усерфриендлинаме.</span><span class="sxs-lookup"><span data-stu-id="e89ed-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-146">**викофмануфактуре**</span><span class="sxs-lookup"><span data-stu-id="e89ed-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-147">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e89ed-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-149">Неделя производства по номеру недели.</span><span class="sxs-lookup"><span data-stu-id="e89ed-149">Week of manufacture by week number.</span></span> <span data-ttu-id="e89ed-150">Диапазон — от 1 до 53.</span><span class="sxs-lookup"><span data-stu-id="e89ed-150">The range is from 1 through 53.</span></span> <span data-ttu-id="e89ed-151">Ноль (0) не определен.</span><span class="sxs-lookup"><span data-stu-id="e89ed-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e89ed-152">**еарофмануфактуре**</span><span class="sxs-lookup"><span data-stu-id="e89ed-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e89ed-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e89ed-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e89ed-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89ed-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e89ed-155">Год изготовления.</span><span class="sxs-lookup"><span data-stu-id="e89ed-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e89ed-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e89ed-156">Remarks</span></span>

<span data-ttu-id="e89ed-157">Обсуждение того, как преобразовать массивы, в которых хранится идентификатор серийного номера, см. в статье [о мониторе отчетов с Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) .</span><span class="sxs-lookup"><span data-stu-id="e89ed-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="e89ed-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="e89ed-158">Examples</span></span>

<span data-ttu-id="e89ed-159">В следующем примере PowerShell извлекается серийный номер нескольких мониторов.</span><span class="sxs-lookup"><span data-stu-id="e89ed-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="e89ed-160">Следующий код VBScript также извлекает сведения об ИДЕНТИФИКАТОРах монитора из системы.</span><span class="sxs-lookup"><span data-stu-id="e89ed-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="e89ed-161">Требования</span><span class="sxs-lookup"><span data-stu-id="e89ed-161">Requirements</span></span>



| <span data-ttu-id="e89ed-162">Требование</span><span class="sxs-lookup"><span data-stu-id="e89ed-162">Requirement</span></span> | <span data-ttu-id="e89ed-163">Значение</span><span class="sxs-lookup"><span data-stu-id="e89ed-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e89ed-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e89ed-164">Minimum supported client</span></span><br/> | <span data-ttu-id="e89ed-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e89ed-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e89ed-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e89ed-166">Minimum supported server</span></span><br/> | <span data-ttu-id="e89ed-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e89ed-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e89ed-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e89ed-168">Namespace</span></span><br/>                | <span data-ttu-id="e89ed-169">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="e89ed-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e89ed-170">MOF</span><span class="sxs-lookup"><span data-stu-id="e89ed-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e89ed-171"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e89ed-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e89ed-172">DLL</span><span class="sxs-lookup"><span data-stu-id="e89ed-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e89ed-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e89ed-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e89ed-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e89ed-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89ed-175">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="e89ed-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

