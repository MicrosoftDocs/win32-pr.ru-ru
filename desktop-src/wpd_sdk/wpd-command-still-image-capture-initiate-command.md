---
description: Команда WPD \_ \_ по- \_ прежнему \_ запускает запись образа \_ . команда initiate инициирует запись образа по прежнему функциональному объекту Image. Если новый объект создается в результате создания изображения, драйвер должен отправить \_ \_ событие добавления объекта события WPD \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Команда WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689488"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="cc57c-104">Команда \_ WPD \_ все \_ еще \_ \_ запускает команду захвата образа</span><span class="sxs-lookup"><span data-stu-id="cc57c-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="cc57c-105">Команда **WPD \_ \_ по- \_ прежнему \_ \_ запускает запись образа** . команда initiate инициирует запись образа по прежнему функциональному объекту Image.</span><span class="sxs-lookup"><span data-stu-id="cc57c-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="cc57c-106">Если новый объект создается в результате создания изображения, драйвер должен отправить событие **\_ \_ \_ добавления объекта события WPD** .</span><span class="sxs-lookup"><span data-stu-id="cc57c-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="cc57c-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="cc57c-107">Command category</span></span>

<span data-ttu-id="cc57c-108">**\_Категория WPD \_ все \_ еще \_ отслеживает образы**</span><span class="sxs-lookup"><span data-stu-id="cc57c-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="cc57c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc57c-109">Parameters</span></span>

<span data-ttu-id="cc57c-110">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="cc57c-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="cc57c-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="cc57c-111">Parameter</span></span>                              | <span data-ttu-id="cc57c-112">VarType</span><span class="sxs-lookup"><span data-stu-id="cc57c-112">VarType</span></span>    | <span data-ttu-id="cc57c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cc57c-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc57c-114">\_ \_ \_ Цель общей команды \_ для свойства WPD</span><span class="sxs-lookup"><span data-stu-id="cc57c-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="cc57c-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cc57c-115">VT\_LPWSTR</span></span> | <span data-ttu-id="cc57c-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cc57c-116">Required.</span></span> <span data-ttu-id="cc57c-117">Идентификатор объекта по прежнему функциональному объекту захвата образа на устройстве, которое должно принимать изображение. Каждый функциональный объект захвата изображений может иметь разные параметры и может ссылаться на другое оборудование на устройстве (например, на переднюю или задней камере телефона), и этот параметр указывает, какой из них следует использовать.</span><span class="sxs-lookup"><span data-stu-id="cc57c-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cc57c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc57c-118">Return Value</span></span>

<span data-ttu-id="cc57c-119">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="cc57c-119">The driver should return the following results.</span></span>



| <span data-ttu-id="cc57c-120">Результат</span><span class="sxs-lookup"><span data-stu-id="cc57c-120">Result</span></span>                                         | <span data-ttu-id="cc57c-121">VarType</span><span class="sxs-lookup"><span data-stu-id="cc57c-121">VarType</span></span>   | <span data-ttu-id="cc57c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="cc57c-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc57c-123">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc57c-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="cc57c-124">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="cc57c-124">VT\_ERROR</span></span> | <span data-ttu-id="cc57c-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cc57c-125">Required.</span></span> <span data-ttu-id="cc57c-126">**Значение HRESULT** , указывающее на успешное выполнение или неудачу выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="cc57c-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="cc57c-127">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **значение HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** и не требуется возвращать какие-либо другие результирующие значения.</span><span class="sxs-lookup"><span data-stu-id="cc57c-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="cc57c-128">Коды ошибок включают в себя [коды ошибок переносных устройств Windows](error-constants.md) или любые другие соответствующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="cc57c-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="cc57c-129">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cc57c-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="cc57c-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="cc57c-130">VT\_UI4</span></span>   | <span data-ttu-id="cc57c-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="cc57c-131">Optional.</span></span> <span data-ttu-id="cc57c-132">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="cc57c-132">A driver-specific error code.</span></span> <span data-ttu-id="cc57c-133">Это значение обычно используется поставщиками устройств для улучшения диагностики ошибок устройства при использовании их приложений.</span><span class="sxs-lookup"><span data-stu-id="cc57c-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="cc57c-134">Приложения общего назначения будут игнорировать его и полагаться исключительно на \_ свойство WPD \_ Common \_ HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cc57c-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="cc57c-135">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="cc57c-135">Calling Methods</span></span>

<span data-ttu-id="cc57c-136">Может вызываться напрямую только с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="cc57c-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc57c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="cc57c-137">Requirements</span></span>



| <span data-ttu-id="cc57c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="cc57c-138">Requirement</span></span> | <span data-ttu-id="cc57c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="cc57c-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc57c-140">Header</span><span class="sxs-lookup"><span data-stu-id="cc57c-140">Header</span></span><br/> | <dl> <span data-ttu-id="cc57c-141"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc57c-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc57c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc57c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc57c-143">**Команды**</span><span class="sxs-lookup"><span data-stu-id="cc57c-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




