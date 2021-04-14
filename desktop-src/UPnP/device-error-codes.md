---
title: Коды ошибок устройства
description: Методы Инвокеактион и Куеристатевариабле возвращают значения HRESULT, которые могут указывать на ошибку устройства (то есть сообщение об ошибке, полученное от устройства, сертифицированного для UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488433"
---
# <a name="device-error-codes"></a><span data-ttu-id="03ad1-103">Коды ошибок устройства</span><span class="sxs-lookup"><span data-stu-id="03ad1-103">Device Error Codes</span></span>

<span data-ttu-id="03ad1-104">Методы [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) и [**куеристатевариабле**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) возвращают значения **HRESULT** , которые могут указывать на ошибку устройства (то есть сообщение об ошибке, полученное от устройства, сертифицированного для UPnP).</span><span class="sxs-lookup"><span data-stu-id="03ad1-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="03ad1-105">При получении ошибки с устройства метод ([**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) или [**куеристатевариабле**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) возвращает значение **HRESULT** , основанное на коде ошибки устройства, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="03ad1-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="03ad1-106">Поскольку преобразование применяется к коду ошибки устройства для получения значения **HRESULT** , код ошибки устройства нельзя считать непосредственно из значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03ad1-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="03ad1-107">Преобразование кода ошибки устройства в значение HRESULT</span><span class="sxs-lookup"><span data-stu-id="03ad1-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="03ad1-108">Существуют стандартные и нестандартные коды ошибок устройств.</span><span class="sxs-lookup"><span data-stu-id="03ad1-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="03ad1-109">Стандартные коды имеют одинаковое значение для всех устройств, сертифицированных с помощью UPnP, и имеют значения менее 600.</span><span class="sxs-lookup"><span data-stu-id="03ad1-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="03ad1-110">Нестандартные коды зависят от поставщика и имеют значения от 600 до 899.</span><span class="sxs-lookup"><span data-stu-id="03ad1-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="03ad1-111">Независимо от того, является ли код ошибки устройства стандартным, определяет способ создания значения **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="03ad1-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="03ad1-112">Стандартный код ошибки устройства сопоставлен со значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03ad1-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="03ad1-113">Нестандартный код ошибки устройства внедряется в значение **HRESULT** путем применения формулы.</span><span class="sxs-lookup"><span data-stu-id="03ad1-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="03ad1-114">Обе эти процедуры можно отменить, чтобы определить код ошибки устройства из определенного значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03ad1-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="03ad1-115">Получение кода ошибки устройства из значения HRESULT</span><span class="sxs-lookup"><span data-stu-id="03ad1-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="03ad1-116">Если значение **HRESULT** больше или равно значению параметра **UPnP \_ e для \_ \_ конкретного действия \_** (0x80040300) и меньше или равно значению параметра max (0x8004042B) **\_ \_ действия \_ \_ UPnP e** , код ошибки устройства является нестандартным — используйте формулу в следующем разделе, чтобы определить код ошибки.</span><span class="sxs-lookup"><span data-stu-id="03ad1-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="03ad1-117">В противном случае код ошибки устройства является стандартным — используйте таблицу в разделе Сопоставление для стандартных кодов ошибок устройства, которая обеспечивает сопоставление значения **HRESULT** с кодом ошибки устройства.</span><span class="sxs-lookup"><span data-stu-id="03ad1-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="03ad1-118">Чтобы получить текстовое описание ошибки после вызова [**иупнпсервице:: инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), задайте для параметра *пварретвал* пустой массив.</span><span class="sxs-lookup"><span data-stu-id="03ad1-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="03ad1-119">После возврата этот параметр будет содержать текстовое описание ошибки, если оно возникло.</span><span class="sxs-lookup"><span data-stu-id="03ad1-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="03ad1-120">Формула для кодов ошибок нестандартного устройства</span><span class="sxs-lookup"><span data-stu-id="03ad1-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="03ad1-121">Используйте следующую формулу, **Если \_ предопределенное действие UPnP e с \_ \_ конкретными действиями \_** ≤ **HRESULT** ≤**UPnP e относится к конкретному \_ \_ \_ \_ максимуму**.</span><span class="sxs-lookup"><span data-stu-id="03ad1-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="03ad1-122">Код ошибки устройства = (**HRESULT**  -  **UPnP \_ E \_ , \_ специфичная \_ для действия**) + **\_ \_ \_ Базовая операция с ошибкой**</span><span class="sxs-lookup"><span data-stu-id="03ad1-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="03ad1-123">При замене фактических числовых значений уравнение имеет значение: код ошибки устройства = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="03ad1-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="03ad1-124">Сопоставление стандартных кодов ошибок устройства</span><span class="sxs-lookup"><span data-stu-id="03ad1-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="03ad1-125">Используйте следующее сопоставление, если   <  **\_ \_ \_ \_ базовое действие HRESULT UPnP E относится к конкретному**.</span><span class="sxs-lookup"><span data-stu-id="03ad1-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="03ad1-126">Значение HRESULT</span><span class="sxs-lookup"><span data-stu-id="03ad1-126">HRESULT value</span></span>                    | <span data-ttu-id="03ad1-127">Код ошибки устройства</span><span class="sxs-lookup"><span data-stu-id="03ad1-127">Device Error Code</span></span>                | <span data-ttu-id="03ad1-128">Фактическое значение</span><span class="sxs-lookup"><span data-stu-id="03ad1-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="03ad1-129">\_ \_ недопустимое действие UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="03ad1-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="03ad1-130">\_неправильное \_ действие</span><span class="sxs-lookup"><span data-stu-id="03ad1-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="03ad1-131">401</span><span class="sxs-lookup"><span data-stu-id="03ad1-131">401</span></span>          |
| <span data-ttu-id="03ad1-132">\_ \_ недопустимые \_ аргументы UPnP E</span><span class="sxs-lookup"><span data-stu-id="03ad1-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="03ad1-133">Недопустимый аргумент "ошибка" \_ \_</span><span class="sxs-lookup"><span data-stu-id="03ad1-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="03ad1-134">402</span><span class="sxs-lookup"><span data-stu-id="03ad1-134">402</span></span>          |
| <span data-ttu-id="03ad1-135">UPNP \_ E \_ не \_ \_ синхронизировано</span><span class="sxs-lookup"><span data-stu-id="03ad1-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="03ad1-136">\_Недопустимый \_ последовательный \_ номер ошибки</span><span class="sxs-lookup"><span data-stu-id="03ad1-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="03ad1-137">403</span><span class="sxs-lookup"><span data-stu-id="03ad1-137">403</span></span>          |
| <span data-ttu-id="03ad1-138">\_ \_ Недопустимая переменная UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="03ad1-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="03ad1-139">Ошибка \_ недопустимой \_ переменной</span><span class="sxs-lookup"><span data-stu-id="03ad1-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="03ad1-140">404</span><span class="sxs-lookup"><span data-stu-id="03ad1-140">404</span></span>          |
| <span data-ttu-id="03ad1-141">\_ \_ \_ сбой запроса действия UPnP \_ E</span><span class="sxs-lookup"><span data-stu-id="03ad1-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="03ad1-142">\_ \_ Внутренняя ошибка устройства \_ сбоя</span><span class="sxs-lookup"><span data-stu-id="03ad1-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="03ad1-143">501</span><span class="sxs-lookup"><span data-stu-id="03ad1-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="03ad1-144">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="03ad1-144">More Information</span></span>

<span data-ttu-id="03ad1-145">Коды ошибок устройства указываются в [архитектуре UPnP для устройств версии 1,0](https://openconnectivity.org/resources/documents.asp).</span><span class="sxs-lookup"><span data-stu-id="03ad1-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="03ad1-146">Константы, упомянутые в этом разделе, определяются в файлах UPnP. h и UPnP. idl.</span><span class="sxs-lookup"><span data-stu-id="03ad1-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




