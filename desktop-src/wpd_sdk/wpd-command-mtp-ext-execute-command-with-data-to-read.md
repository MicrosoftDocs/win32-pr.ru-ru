---
description: Команда WPD \_ \_ MTP \_ EXECUTE команда \_ \_ \_ с \_ данными \_ для \_ чтения отправляет блок команд MTP, за которым следует фаза данных. (Данные отправляются с устройства на узел.)
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Команда WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708387"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="cdcd4-104">Команда \_ WPD \_ MTP \_ \_ EXECUTE команда \_ \_ с \_ данными \_ для \_ чтения команда</span><span class="sxs-lookup"><span data-stu-id="cdcd4-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="cdcd4-105">Команда **WPD \_ \_ MTP \_ EXECUTE команда \_ \_ \_ с \_ данными \_ для \_ чтения** отправляет блок команд MTP, за которым следует фаза данных.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="cdcd4-106">(Данные отправляются с устройства на узел.)</span><span class="sxs-lookup"><span data-stu-id="cdcd4-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="cdcd4-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="cdcd4-107">Command category</span></span>

<span data-ttu-id="cdcd4-108">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="cdcd4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdcd4-109">Parameters</span></span>

<span data-ttu-id="cdcd4-110">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="cdcd4-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="cdcd4-111">Parameter</span></span>                                      | <span data-ttu-id="cdcd4-112">VarType</span><span class="sxs-lookup"><span data-stu-id="cdcd4-112">VarType</span></span> | <span data-ttu-id="cdcd4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cdcd4-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcd4-114">**\_свойство WPD \_ \_ \_ код операции MTP \_**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="cdcd4-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="cdcd4-115">VT\_UI4</span></span> | <span data-ttu-id="cdcd4-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-116">Required.</span></span> <span data-ttu-id="cdcd4-117">Идентифицирует код операции, расширенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="cdcd4-118">**\_Свойства WPD \_ для \_ \_ параметров операции ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="cdcd4-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="cdcd4-119">VT\_UI4</span></span> | <span data-ttu-id="cdcd4-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-120">Required.</span></span> <span data-ttu-id="cdcd4-121">Объект **ипортабледевицепропвариантколлектион**, который определяет обязательные параметры для кода операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="cdcd4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdcd4-122">Return Value</span></span>

<span data-ttu-id="cdcd4-123">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-123">The driver returns the following results.</span></span>



| <span data-ttu-id="cdcd4-124">Результат</span><span class="sxs-lookup"><span data-stu-id="cdcd4-124">Result</span></span>                                                       | <span data-ttu-id="cdcd4-125">VarType</span><span class="sxs-lookup"><span data-stu-id="cdcd4-125">VarType</span></span>    | <span data-ttu-id="cdcd4-126">Описание</span><span class="sxs-lookup"><span data-stu-id="cdcd4-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcd4-127">**Свойство WPD " \_ \_ MTP \_ ext \_ передает \_ Общий \_ \_ Размер данных"**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="cdcd4-128">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="cdcd4-128">VT\_UI8</span></span>    | <span data-ttu-id="cdcd4-129">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-129">Required.</span></span> <span data-ttu-id="cdcd4-130">Возвращает общий объем данных в байтах, за исключением любых издержек, поступающих от устройства.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="cdcd4-131">Если устройство сообщает о неизвестном размере данных (0xFFFFFFFF), драйвер должен повторно вызывать **ReadData** до получения короткого фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="cdcd4-132">**\_свойство WPD \_ . \_ \_ оптимальный \_ \_ Размер буфера \_ перемещения MTP**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="cdcd4-133">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="cdcd4-133">VT\_UI4</span></span>    | <span data-ttu-id="cdcd4-134">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-134">Optional.</span></span> <span data-ttu-id="cdcd4-135">Возвращает оптимальный размер буфера перемещения.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="cdcd4-136">**\_свойство WPD \_ для \_ \_ контекста перемещения \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="cdcd4-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="cdcd4-137">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cdcd4-137">VT\_LPWSTR</span></span> | <span data-ttu-id="cdcd4-138">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-138">Required.</span></span> <span data-ttu-id="cdcd4-139">Указывает идентификатор контекста для последующих передач данных.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="cdcd4-140">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="cdcd4-140">Calling Methods</span></span>

<span data-ttu-id="cdcd4-141">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="cdcd4-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcd4-142">Требования</span><span class="sxs-lookup"><span data-stu-id="cdcd4-142">Requirements</span></span>



| <span data-ttu-id="cdcd4-143">Требование</span><span class="sxs-lookup"><span data-stu-id="cdcd4-143">Requirement</span></span> | <span data-ttu-id="cdcd4-144">Значение</span><span class="sxs-lookup"><span data-stu-id="cdcd4-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcd4-145">Header</span><span class="sxs-lookup"><span data-stu-id="cdcd4-145">Header</span></span><br/> | <dl> <span data-ttu-id="cdcd4-146"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdcd4-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcd4-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdcd4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcd4-148">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="cdcd4-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




