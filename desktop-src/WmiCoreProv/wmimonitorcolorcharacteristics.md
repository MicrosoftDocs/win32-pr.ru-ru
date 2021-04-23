---
description: Представляет характеристики цвета "Международная комиссия по освещения (ЦИЕ)" монитора компьютера.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Класс Вмимониторколорчарактеристикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346505"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="291c4-103">Класс Вмимониторколорчарактеристикс</span><span class="sxs-lookup"><span data-stu-id="291c4-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="291c4-104">Класс **вмимониторколорчарактеристикс** представляет характеристики цвета международной комиссии по освещения (Цие) монитора компьютера.</span><span class="sxs-lookup"><span data-stu-id="291c4-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="291c4-105">Данные соответствуют данным в блоке цветовых характеристик для расширенной структуры расширенных отображаемых идентификационных данных (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="291c4-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="291c4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="291c4-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="291c4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="291c4-107">Members</span></span>

<span data-ttu-id="291c4-108">Класс **вмимониторколорчарактеристикс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="291c4-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="291c4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="291c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="291c4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="291c4-110">Properties</span></span>

<span data-ttu-id="291c4-111">Класс **вмимониторколорчарактеристикс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="291c4-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="291c4-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="291c4-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="291c4-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="291c4-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="291c4-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="291c4-116">**Синий**</span><span class="sxs-lookup"><span data-stu-id="291c4-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-117">Тип данных: **[ **ксизинЦие**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="291c4-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="291c4-119">ЦИЕ координаты синего, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="291c4-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="291c4-120">**дефаултвхите**</span><span class="sxs-lookup"><span data-stu-id="291c4-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-121">Тип данных: **[ **ксизинЦие**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="291c4-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="291c4-123">Белые координаты ЦИЕ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="291c4-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="291c4-124">**Зеленый**</span><span class="sxs-lookup"><span data-stu-id="291c4-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-125">Тип данных: **[ **ксизинЦие**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="291c4-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="291c4-127">ЦИЕ координаты зеленого цвета, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="291c4-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="291c4-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="291c4-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="291c4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="291c4-131">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="291c4-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="291c4-132">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="291c4-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="291c4-133">**Красный**</span><span class="sxs-lookup"><span data-stu-id="291c4-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="291c4-134">Тип данных: **[ **ксизинЦие**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="291c4-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="291c4-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="291c4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="291c4-136">ЦИЕ координаты красного, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="291c4-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="291c4-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="291c4-137">Remarks</span></span>

<span data-ttu-id="291c4-138">Значения «Цветность» и «белая точка» выражаются в виде дробных чисел в формате кодировки.</span><span class="sxs-lookup"><span data-stu-id="291c4-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="291c4-139">Этот формат является точным для тысячового расположения, длина которого равна 10 битам.</span><span class="sxs-lookup"><span data-stu-id="291c4-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="291c4-140">Самый значащий бит (старший) представляет 2 ^-1, а наименьший значащий бит (ЛСБ) представляет 2 ^-10 коэффициенты соответственно.</span><span class="sxs-lookup"><span data-stu-id="291c4-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="291c4-141">Точность сохраненных значений в структуре E-EDID v1. x должна быть точной до +/-0,005 фактического значения.</span><span class="sxs-lookup"><span data-stu-id="291c4-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="291c4-142">Требования</span><span class="sxs-lookup"><span data-stu-id="291c4-142">Requirements</span></span>



| <span data-ttu-id="291c4-143">Требование</span><span class="sxs-lookup"><span data-stu-id="291c4-143">Requirement</span></span> | <span data-ttu-id="291c4-144">Значение</span><span class="sxs-lookup"><span data-stu-id="291c4-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="291c4-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="291c4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="291c4-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="291c4-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="291c4-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="291c4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="291c4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="291c4-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="291c4-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="291c4-149">Namespace</span></span><br/>                | <span data-ttu-id="291c4-150">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="291c4-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="291c4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="291c4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="291c4-152"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="291c4-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="291c4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="291c4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="291c4-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="291c4-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="291c4-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="291c4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291c4-156">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="291c4-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




