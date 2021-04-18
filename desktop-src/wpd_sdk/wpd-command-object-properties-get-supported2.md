---
description: Извлекает свойства, поддерживаемые объектом.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Команда WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718045"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="450c3-103">\_ \_ \_ \_ Поддерживаемые команды в СВОЙСТВАх объекта команды WPD \_</span><span class="sxs-lookup"><span data-stu-id="450c3-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="450c3-104">Команда **WPD \_ : \_ свойства объекта команды " \_ \_ получить \_ поддерживаемый** " возвращает свойства, поддерживаемые объектом.</span><span class="sxs-lookup"><span data-stu-id="450c3-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="450c3-105">Категория команды</span><span class="sxs-lookup"><span data-stu-id="450c3-105">Command Category</span></span>

<span data-ttu-id="450c3-106">**\_ \_ свойства объекта категории \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="450c3-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="450c3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="450c3-107">Parameters</span></span>

<span data-ttu-id="450c3-108">Драйверу необходим следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="450c3-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="450c3-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="450c3-109">Parameter</span></span>                                         | <span data-ttu-id="450c3-110">VarType</span><span class="sxs-lookup"><span data-stu-id="450c3-110">VarType</span></span>        | <span data-ttu-id="450c3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="450c3-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="450c3-112">**\_ \_ \_ \_ идентификатор объекта свойств объекта свойства \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="450c3-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="450c3-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="450c3-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="450c3-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="450c3-114">Required.</span></span> <span data-ttu-id="450c3-115">Идентификатор объекта, который содержит запрошенные свойства.</span><span class="sxs-lookup"><span data-stu-id="450c3-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="450c3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="450c3-116">Return Value</span></span>

<span data-ttu-id="450c3-117">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="450c3-117">The driver should return the following results.</span></span>



| <span data-ttu-id="450c3-118">Результат</span><span class="sxs-lookup"><span data-stu-id="450c3-118">Result</span></span>                                                | <span data-ttu-id="450c3-119">VarType</span><span class="sxs-lookup"><span data-stu-id="450c3-119">VarType</span></span>         | <span data-ttu-id="450c3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="450c3-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450c3-121">**\_ \_ свойства объекта свойства \_ WPD \_ \_ ключи свойств**</span><span class="sxs-lookup"><span data-stu-id="450c3-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="450c3-122">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="450c3-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="450c3-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="450c3-123">Required.</span></span> <span data-ttu-id="450c3-124">Интерфейс [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , указывающий все поддерживаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="450c3-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="450c3-125">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="450c3-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="450c3-126">**\_Ошибка VT**</span><span class="sxs-lookup"><span data-stu-id="450c3-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="450c3-127">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="450c3-127">Required.</span></span> <span data-ttu-id="450c3-128">Значение **HRESULT** , указывающее общее число успешных или неудачных попыток.</span><span class="sxs-lookup"><span data-stu-id="450c3-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="450c3-129">Возможные значения результата включают в себя [коды ошибок переносных устройств Windows](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="450c3-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="450c3-130">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** , но в противном случае не требуется возвращать какое-либо другое результирующее значение.</span><span class="sxs-lookup"><span data-stu-id="450c3-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="450c3-131">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="450c3-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="450c3-132">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="450c3-132">**VT\_UI4**</span></span>     | <span data-ttu-id="450c3-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="450c3-133">Optional.</span></span> <span data-ttu-id="450c3-134">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="450c3-134">A driver-specific error code.</span></span> <span data-ttu-id="450c3-135">Обычно это используется только для тестирования драйверов или, если все драйверы, устройства и клиенты разработаны вместе.</span><span class="sxs-lookup"><span data-stu-id="450c3-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="450c3-136">Требования</span><span class="sxs-lookup"><span data-stu-id="450c3-136">Requirements</span></span>



| <span data-ttu-id="450c3-137">Требование</span><span class="sxs-lookup"><span data-stu-id="450c3-137">Requirement</span></span> | <span data-ttu-id="450c3-138">Значение</span><span class="sxs-lookup"><span data-stu-id="450c3-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="450c3-139">Header</span><span class="sxs-lookup"><span data-stu-id="450c3-139">Header</span></span><br/> | <dl> <span data-ttu-id="450c3-140"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="450c3-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450c3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="450c3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450c3-142">**Команды**</span><span class="sxs-lookup"><span data-stu-id="450c3-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




