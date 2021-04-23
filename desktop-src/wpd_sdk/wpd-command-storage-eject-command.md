---
description: Команда WPD \_ \_ Storage команда \_ Eject извлекает носитель, который можно удаленно извлечь с компьютера.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Команда WPD_COMMAND_STORAGE_EJECT (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648883"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="e0e56-103">\_Команда для \_ хранилища \_ команд WPD</span><span class="sxs-lookup"><span data-stu-id="e0e56-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="e0e56-104">Команда **WPD \_ \_ Storage команда \_ Eject** извлекает носитель, который можно удаленно извлечь с компьютера.</span><span class="sxs-lookup"><span data-stu-id="e0e56-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="e0e56-105">Категория команды</span><span class="sxs-lookup"><span data-stu-id="e0e56-105">Command category</span></span>

<span data-ttu-id="e0e56-106">**\_хранилище категорий \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e0e56-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="e0e56-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0e56-107">Parameters</span></span>

<span data-ttu-id="e0e56-108">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e0e56-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="e0e56-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="e0e56-109">Parameter</span></span>                          | <span data-ttu-id="e0e56-110">VarType</span><span class="sxs-lookup"><span data-stu-id="e0e56-110">VarType</span></span>    | <span data-ttu-id="e0e56-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e0e56-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="e0e56-112">\_ \_ \_ идентификатор объекта хранилища свойств \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e0e56-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="e0e56-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e0e56-113">VT\_LPWSTR</span></span> | <span data-ttu-id="e0e56-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e0e56-114">Required.</span></span> <span data-ttu-id="e0e56-115">Идентификатор объекта объекта хранилища, который необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="e0e56-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="e0e56-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0e56-116">Return Value</span></span>

<span data-ttu-id="e0e56-117">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="e0e56-117">The driver should return the following results.</span></span>



| <span data-ttu-id="e0e56-118">Результат</span><span class="sxs-lookup"><span data-stu-id="e0e56-118">Result</span></span>                                         | <span data-ttu-id="e0e56-119">VarType</span><span class="sxs-lookup"><span data-stu-id="e0e56-119">VarType</span></span>   | <span data-ttu-id="e0e56-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e0e56-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e56-121">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e0e56-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="e0e56-122">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="e0e56-122">VT\_ERROR</span></span> | <span data-ttu-id="e0e56-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e0e56-123">Required.</span></span> <span data-ttu-id="e0e56-124">**Значение HRESULT** , указывающее на успешное выполнение или неудачу выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="e0e56-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="e0e56-125">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **значение HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** и не требуется возвращать какие-либо другие результирующие значения.</span><span class="sxs-lookup"><span data-stu-id="e0e56-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="e0e56-126">Коды ошибок включают в себя [коды ошибок переносных устройств Windows](error-constants.md) или любые другие соответствующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="e0e56-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="e0e56-127">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e0e56-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="e0e56-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e0e56-128">VT\_UI4</span></span>   | <span data-ttu-id="e0e56-129">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e0e56-129">Optional.</span></span> <span data-ttu-id="e0e56-130">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="e0e56-130">A driver-specific error code.</span></span> <span data-ttu-id="e0e56-131">Обычно это используется только для тестирования драйверов или, если все драйверы, устройства и клиенты разработаны вместе.</span><span class="sxs-lookup"><span data-stu-id="e0e56-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="e0e56-132">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="e0e56-132">Calling Methods</span></span>

<span data-ttu-id="e0e56-133">Может вызываться напрямую только с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="e0e56-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e56-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e0e56-134">Requirements</span></span>



| <span data-ttu-id="e0e56-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e0e56-135">Requirement</span></span> | <span data-ttu-id="e0e56-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e0e56-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e56-137">Header</span><span class="sxs-lookup"><span data-stu-id="e0e56-137">Header</span></span><br/> | <dl> <span data-ttu-id="e0e56-138"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e56-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e56-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0e56-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e56-140">**Команды**</span><span class="sxs-lookup"><span data-stu-id="e0e56-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




