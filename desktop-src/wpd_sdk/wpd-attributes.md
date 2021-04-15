---
description: Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты параметров для методов и событий службы устройства.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Атрибуты параметров (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714083"
---
# <a name="parameter-attributes"></a><span data-ttu-id="05888-103">Атрибуты параметра</span><span class="sxs-lookup"><span data-stu-id="05888-103">Parameter Attributes</span></span>

<span data-ttu-id="05888-104">Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты параметров для методов и событий службы устройства.</span><span class="sxs-lookup"><span data-stu-id="05888-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="05888-105">Эти атрибуты возвращаются следующими методами:</span><span class="sxs-lookup"><span data-stu-id="05888-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="05888-106">**Ипортабледевицесервицекапабилитиес:: Жетмесодпараметераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="05888-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="05888-107">**Ипортабледевицесервицекапабилитиес:: Жетевентпараметераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="05888-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="05888-108">attribute</span><span class="sxs-lookup"><span data-stu-id="05888-108">Attribute</span></span>                                            | <span data-ttu-id="05888-109">VarType</span><span class="sxs-lookup"><span data-stu-id="05888-109">VarType</span></span>         | <span data-ttu-id="05888-110">Описание</span><span class="sxs-lookup"><span data-stu-id="05888-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05888-111">**\_ \_ значение атрибута параметра WPD \_ по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="05888-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="05888-112">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="05888-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="05888-113">Значение параметра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05888-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="05888-114">**\_ \_ \_ элементы ПЕРЕЧИСЛЕНИЯ атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="05888-115">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="05888-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="05888-116">Интерфейс [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который содержит значения перечисления для параметра.</span><span class="sxs-lookup"><span data-stu-id="05888-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="05888-117">**\_ \_ форма атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="05888-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="05888-118">**VT\_UI4**</span></span>     | <span data-ttu-id="05888-119">Допустимая форма допустимых значений параметров.</span><span class="sxs-lookup"><span data-stu-id="05888-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="05888-120">**\_ \_ \_ максимальный \_ Размер атрибута параметра WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="05888-121">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="05888-121">**VT\_UI8**</span></span>     | <span data-ttu-id="05888-122">Максимальный размер параметра в байтах.</span><span class="sxs-lookup"><span data-stu-id="05888-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="05888-123">**\_ \_ имя атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="05888-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05888-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="05888-125">Строка, указывающая понятное для сценария имя параметра события или метода.</span><span class="sxs-lookup"><span data-stu-id="05888-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="05888-126">Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ".</span><span class="sxs-lookup"><span data-stu-id="05888-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="05888-127">**\_ \_ порядок АТРИБУТОВ параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="05888-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="05888-128">**VT\_UI4**</span></span>     | <span data-ttu-id="05888-129">Индекс порядка параметров (с отсчетом от нуля), чтобы значение порядка 0 соответствовало первому параметру.</span><span class="sxs-lookup"><span data-stu-id="05888-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="05888-130">**\_ \_ \_ мин диапазон атрибутов параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="05888-131">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="05888-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="05888-132">Максимальное значение для параметра в виде \_ \_ диапазона формы атрибута параметра WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="05888-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="05888-133">**\_ \_ \_ максимальный диапазон атрибутов параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="05888-134">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="05888-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="05888-135">Минимальное значение параметра формы \_ атрибута параметра типа WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="05888-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="05888-136">**\_ \_ \_ шаг диапазона атрибутов параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="05888-137">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="05888-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="05888-138">Значение шага для параметра формы атрибута параметра в формате WPD \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="05888-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="05888-139">**\_ \_ \_ регулярное выражение атрибута параметра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="05888-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="05888-140">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05888-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="05888-141">Регулярное выражение, задающее допустимые значения параметров формы \_ атрибута параметра WPD \_ в \_ виде \_ регулярного \_ выражения.</span><span class="sxs-lookup"><span data-stu-id="05888-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="05888-142">**\_ \_ \_ тип использования атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="05888-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="05888-143">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="05888-143">**VT\_UI4**</span></span>     | <span data-ttu-id="05888-144">Целое число, задающее использование параметра метода, например, в/из. Допустимые значения — тип [**перечисления \_ \_ \_ типов использования параметра WPD**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="05888-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="05888-145">**\_ \_ атрибут VarType для параметра с ПАРАМЕТРом WPD \_**</span><span class="sxs-lookup"><span data-stu-id="05888-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="05888-146">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="05888-146">**VT\_UI4**</span></span>     | <span data-ttu-id="05888-147">Параметр VarType.</span><span class="sxs-lookup"><span data-stu-id="05888-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="05888-148">Требования</span><span class="sxs-lookup"><span data-stu-id="05888-148">Requirements</span></span>



| <span data-ttu-id="05888-149">Требование</span><span class="sxs-lookup"><span data-stu-id="05888-149">Requirement</span></span> | <span data-ttu-id="05888-150">Значение</span><span class="sxs-lookup"><span data-stu-id="05888-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="05888-151">Header</span><span class="sxs-lookup"><span data-stu-id="05888-151">Header</span></span><br/> | <dl> <span data-ttu-id="05888-152"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="05888-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05888-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05888-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05888-154">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="05888-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




