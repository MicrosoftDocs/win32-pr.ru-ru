---
description: Команда WPD \_ \_ Device \_ Location указания по \_ получению \_ содержимого \_ возвращает идентификаторы объектов папок, которые могут содержать объект указанного типа.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Команда WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704147"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="b591a-103">WPD \_ Command \_ Device \_ указания \_ о \_ получении \_ расположения содержимого команда</span><span class="sxs-lookup"><span data-stu-id="b591a-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="b591a-104">Команда **WPD \_ \_ Device \_ Location указания по \_ получению \_ содержимого \_** возвращает идентификаторы объектов папок, которые могут содержать объект указанного типа.</span><span class="sxs-lookup"><span data-stu-id="b591a-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="b591a-105">Эта команда предоставляет клиенту более быстрый способ обнаружения места, в котором устройство хранит определенные объекты, чем перечисление объектов методом подбора.</span><span class="sxs-lookup"><span data-stu-id="b591a-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="b591a-106">Категория команды</span><span class="sxs-lookup"><span data-stu-id="b591a-106">Command category</span></span>

<span data-ttu-id="b591a-107">**\_указания для \_ устройств \_ категории WPD**</span><span class="sxs-lookup"><span data-stu-id="b591a-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="b591a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b591a-108">Parameters</span></span>

<span data-ttu-id="b591a-109">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="b591a-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="b591a-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="b591a-110">Parameter</span></span>                                   | <span data-ttu-id="b591a-111">VarType</span><span class="sxs-lookup"><span data-stu-id="b591a-111">VarType</span></span>   | <span data-ttu-id="b591a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b591a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b591a-113">\_ \_ \_ тип содержимого "подсказки \_ " для свойства устройства WPD \_</span><span class="sxs-lookup"><span data-stu-id="b591a-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="b591a-114">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="b591a-114">VT\_CLSID</span></span> | <span data-ttu-id="b591a-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b591a-115">Required.</span></span> <span data-ttu-id="b591a-116">Тип объекта, для которого вызывающий объект хочет найти контейнер.</span><span class="sxs-lookup"><span data-stu-id="b591a-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="b591a-117">Например, чтобы найти папки верхнего уровня, используемые для хранения изображений на цифровой камере, вызывающий объект будет отправлять \_ изображение типа содержимого WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b591a-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="b591a-118">Список типов объектов, определенных портативными устройствами Windows, см. в разделе [требования для объектов](requirements-for-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="b591a-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="b591a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b591a-119">Return Value</span></span>

<span data-ttu-id="b591a-120">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="b591a-120">The driver should return the following results.</span></span>



| <span data-ttu-id="b591a-121">Результат</span><span class="sxs-lookup"><span data-stu-id="b591a-121">Result</span></span>                                               | <span data-ttu-id="b591a-122">VarType</span><span class="sxs-lookup"><span data-stu-id="b591a-122">VarType</span></span>     | <span data-ttu-id="b591a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b591a-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b591a-124">**\_Свойства WPD \_ устройства \_ указания \_ \_ расположения содержимого**</span><span class="sxs-lookup"><span data-stu-id="b591a-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="b591a-125">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="b591a-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="b591a-126">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b591a-126">Required.</span></span> <span data-ttu-id="b591a-127">[**Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) типа VT \_ LPWSTR, задающих идентификаторы объектов папок, содержащих объекты типа, указанного в параметре вызова.</span><span class="sxs-lookup"><span data-stu-id="b591a-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="b591a-128">Если папки не найдены, это должен быть пустой список. Папки, указанные в результате, могут не содержать объектов других типов содержимого.</span><span class="sxs-lookup"><span data-stu-id="b591a-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="b591a-129">Сведения об ограничениях для папок см. в свойстве " [ \_ \_ \_ \_ Разрешенные типы содержимого папки WPD](miscellaneous-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="b591a-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="b591a-130">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b591a-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="b591a-131">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="b591a-131">VT\_ERROR</span></span>   | <span data-ttu-id="b591a-132">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b591a-132">Required.</span></span> <span data-ttu-id="b591a-133">**Значение HRESULT** , указывающее на успешное выполнение или ошибку при обработке команды.</span><span class="sxs-lookup"><span data-stu-id="b591a-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="b591a-134">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **значение HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** и не требуется возвращать какие-либо другие результирующие значения.</span><span class="sxs-lookup"><span data-stu-id="b591a-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="b591a-135">Коды ошибок включают в себя [коды ошибок переносных устройств Windows](error-constants.md) или любые другие соответствующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="b591a-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b591a-136">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b591a-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="b591a-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b591a-137">VT\_UI4</span></span>     | <span data-ttu-id="b591a-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b591a-138">Optional.</span></span> <span data-ttu-id="b591a-139">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="b591a-139">A driver-specific error code.</span></span> <span data-ttu-id="b591a-140">Обычно это используется только для тестирования драйверов или, если все драйверы, устройства и клиенты разработаны вместе.</span><span class="sxs-lookup"><span data-stu-id="b591a-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="b591a-141">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="b591a-141">Calling Methods</span></span>

<span data-ttu-id="b591a-142">Может вызываться напрямую только с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="b591a-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="b591a-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b591a-143">Requirements</span></span>



| <span data-ttu-id="b591a-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b591a-144">Requirement</span></span> | <span data-ttu-id="b591a-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b591a-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b591a-146">Header</span><span class="sxs-lookup"><span data-stu-id="b591a-146">Header</span></span><br/> | <dl> <span data-ttu-id="b591a-147"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="b591a-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




