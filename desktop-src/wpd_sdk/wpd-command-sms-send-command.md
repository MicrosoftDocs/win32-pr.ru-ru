---
description: Команда WPD \_ \_ SMS \_ Send инициирует ОТправку SMS-сообщения от функционального объекта SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Команда WPD_COMMAND_SMS_SEND (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717845"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="4197f-103">Команда WPD команда \_ \_ \_ Send SMS</span><span class="sxs-lookup"><span data-stu-id="4197f-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="4197f-104">Команда **WPD \_ \_ SMS \_ Send** инициирует отправку SMS-сообщения от функционального объекта SMS.</span><span class="sxs-lookup"><span data-stu-id="4197f-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="4197f-105">Категория команды</span><span class="sxs-lookup"><span data-stu-id="4197f-105">Command category</span></span>

<span data-ttu-id="4197f-106">**\_Категория WPD \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="4197f-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="4197f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4197f-107">Parameters</span></span>

<span data-ttu-id="4197f-108">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="4197f-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="4197f-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="4197f-109">Parameter</span></span>                              | <span data-ttu-id="4197f-110">VarType</span><span class="sxs-lookup"><span data-stu-id="4197f-110">VarType</span></span>             | <span data-ttu-id="4197f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4197f-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4197f-112">\_ \_ \_ Цель общей команды \_ для свойства WPD</span><span class="sxs-lookup"><span data-stu-id="4197f-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="4197f-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4197f-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="4197f-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4197f-114">Required.</span></span> <span data-ttu-id="4197f-115">Идентификатор объекта для функционального объекта SMS, который должен отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="4197f-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="4197f-116">Различные функциональные объекты SMS могут иметь разные параметры.</span><span class="sxs-lookup"><span data-stu-id="4197f-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="4197f-117">\_ \_ получатель SMS свойства \_ WPD</span><span class="sxs-lookup"><span data-stu-id="4197f-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="4197f-118">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4197f-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="4197f-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4197f-119">Required.</span></span> <span data-ttu-id="4197f-120">Универсальный код ресурса (URI) получателя.</span><span class="sxs-lookup"><span data-stu-id="4197f-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="4197f-121">\_ \_ \_ тип сообщения SMS свойства \_ WPD</span><span class="sxs-lookup"><span data-stu-id="4197f-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="4197f-122">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4197f-122">VT\_UI4</span></span>             | <span data-ttu-id="4197f-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4197f-123">Required.</span></span> <span data-ttu-id="4197f-124">Перечислитель [**\_ \_ типов SMS-сообщений**](sms-message-types.md) , указывающий тип сообщения (текстовый или двоичный).</span><span class="sxs-lookup"><span data-stu-id="4197f-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="4197f-125">\_SMS, \_ \_ ТЕКСТОВОЕ \_ сообщение свойства WPD</span><span class="sxs-lookup"><span data-stu-id="4197f-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="4197f-126">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4197f-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="4197f-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4197f-127">Optional.</span></span> <span data-ttu-id="4197f-128">Если **\_ \_ \_ \_ тип сообщения SMS свойства WPD** указывает текстовое сообщение, это строка сообщения; в противном случае этот параметр не включается.</span><span class="sxs-lookup"><span data-stu-id="4197f-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="4197f-129">\_ \_ \_ двоичное сообщение свойства WPD SMS \_</span><span class="sxs-lookup"><span data-stu-id="4197f-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="4197f-130">VT \_ вектор \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="4197f-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="4197f-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4197f-131">Optional.</span></span> <span data-ttu-id="4197f-132">Если **\_ \_ \_ \_ тип сообщения SMS свойства WPD** указывает на двоичное сообщение, это указатель на массив байтов; в противном случае этот параметр не включается.</span><span class="sxs-lookup"><span data-stu-id="4197f-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="4197f-133">Первый DWORD значения — это длина массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="4197f-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="4197f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4197f-134">Return Value</span></span>

<span data-ttu-id="4197f-135">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="4197f-135">The driver should return the following results.</span></span>



| <span data-ttu-id="4197f-136">Результат</span><span class="sxs-lookup"><span data-stu-id="4197f-136">Result</span></span>                                         | <span data-ttu-id="4197f-137">VarType</span><span class="sxs-lookup"><span data-stu-id="4197f-137">VarType</span></span>   | <span data-ttu-id="4197f-138">Описание</span><span class="sxs-lookup"><span data-stu-id="4197f-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4197f-139">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4197f-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="4197f-140">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="4197f-140">VT\_ERROR</span></span> | <span data-ttu-id="4197f-141">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4197f-141">Required.</span></span> <span data-ttu-id="4197f-142">**Значение HRESULT** , указывающее на успешное выполнение или неудачу выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="4197f-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="4197f-143">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **значение HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** и не требуется возвращать какие-либо другие результирующие значения.</span><span class="sxs-lookup"><span data-stu-id="4197f-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="4197f-144">Коды ошибок включают в себя [коды ошибок переносных устройств Windows](error-constants.md) или любые другие соответствующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4197f-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="4197f-145">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="4197f-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="4197f-146">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4197f-146">VT\_UI4</span></span>   | <span data-ttu-id="4197f-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4197f-147">Optional.</span></span> <span data-ttu-id="4197f-148">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="4197f-148">A driver-specific error code.</span></span> <span data-ttu-id="4197f-149">Обычно это используется только для тестирования драйверов или, если все драйверы, устройства и клиенты разработаны вместе.</span><span class="sxs-lookup"><span data-stu-id="4197f-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="4197f-150">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="4197f-150">Calling Methods</span></span>

<span data-ttu-id="4197f-151">Может вызываться напрямую только с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="4197f-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="4197f-152">Требования</span><span class="sxs-lookup"><span data-stu-id="4197f-152">Requirements</span></span>



| <span data-ttu-id="4197f-153">Требование</span><span class="sxs-lookup"><span data-stu-id="4197f-153">Requirement</span></span> | <span data-ttu-id="4197f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="4197f-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4197f-155">Header</span><span class="sxs-lookup"><span data-stu-id="4197f-155">Header</span></span><br/> | <dl> <span data-ttu-id="4197f-156"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="4197f-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4197f-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4197f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4197f-158">**Команды**</span><span class="sxs-lookup"><span data-stu-id="4197f-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




