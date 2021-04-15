---
description: Команда WPD \_ \_ \_ \_ , выполняемая командой \_ MTP \_ с командой \_ данных \_ для \_ записи, отправляет блок команд MTP, за которым следует фаза данных. Данные отправляются с узла на устройство.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Команда WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708386"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="210dd-104">Команда WPD команды " \_ \_ MTP" выполнить команду \_ \_ \_ \_ с \_ данными \_ для \_ записи</span><span class="sxs-lookup"><span data-stu-id="210dd-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="210dd-105">Команда **WPD \_ , \_ \_ выполняемая командой MTP \_ с командой \_ \_ \_ данных \_ для \_ записи** , отправляет блок команд MTP, за которым следует фаза данных.</span><span class="sxs-lookup"><span data-stu-id="210dd-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="210dd-106">Данные отправляются с узла на устройство.</span><span class="sxs-lookup"><span data-stu-id="210dd-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="210dd-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="210dd-107">Command category</span></span>

<span data-ttu-id="210dd-108">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="210dd-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="210dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="210dd-109">Parameters</span></span>

<span data-ttu-id="210dd-110">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="210dd-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="210dd-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="210dd-111">Parameter</span></span>                                                | <span data-ttu-id="210dd-112">VarType</span><span class="sxs-lookup"><span data-stu-id="210dd-112">VarType</span></span> | <span data-ttu-id="210dd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="210dd-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210dd-114">**\_свойство WPD \_ \_ \_ код операции MTP \_**</span><span class="sxs-lookup"><span data-stu-id="210dd-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="210dd-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="210dd-115">VT\_UI4</span></span> | <span data-ttu-id="210dd-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="210dd-116">Required.</span></span> <span data-ttu-id="210dd-117">Идентифицирует код операции, расширенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="210dd-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="210dd-118">**\_Свойства WPD \_ для \_ \_ параметров операции ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="210dd-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="210dd-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="210dd-119">VT\_UI4</span></span> | <span data-ttu-id="210dd-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="210dd-120">Required.</span></span> <span data-ttu-id="210dd-121">Коллекция **ипортабледевицепропвариантколлектион** , которая определяет необходимые параметры для кода операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="210dd-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="210dd-122">**Свойство WPD " \_ \_ MTP \_ ext \_ передает \_ Общий \_ \_ Размер данных"**</span><span class="sxs-lookup"><span data-stu-id="210dd-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="210dd-123">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="210dd-123">VT\_UI8</span></span> | <span data-ttu-id="210dd-124">Обязательный параметр. указывает общий объем данных в байтах, исключая любые издержки, отправляемые на устройство.</span><span class="sxs-lookup"><span data-stu-id="210dd-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="210dd-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="210dd-125">Return Value</span></span>

<span data-ttu-id="210dd-126">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="210dd-126">The driver returns the following results.</span></span>



| <span data-ttu-id="210dd-127">Результат</span><span class="sxs-lookup"><span data-stu-id="210dd-127">Result</span></span>                                                       | <span data-ttu-id="210dd-128">VarType</span><span class="sxs-lookup"><span data-stu-id="210dd-128">VarType</span></span>    | <span data-ttu-id="210dd-129">Описание</span><span class="sxs-lookup"><span data-stu-id="210dd-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="210dd-130">**\_свойство WPD \_ . \_ \_ оптимальный \_ \_ Размер буфера \_ перемещения MTP**</span><span class="sxs-lookup"><span data-stu-id="210dd-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="210dd-131">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="210dd-131">VT\_UI4</span></span>    | <span data-ttu-id="210dd-132">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="210dd-132">Required.</span></span> <span data-ttu-id="210dd-133">Задает оптимальный размер буфера перемещения.</span><span class="sxs-lookup"><span data-stu-id="210dd-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="210dd-134">**\_свойство WPD \_ для \_ \_ контекста перемещения \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="210dd-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="210dd-135">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="210dd-135">VT\_LPWSTR</span></span> | <span data-ttu-id="210dd-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="210dd-136">Optional.</span></span> <span data-ttu-id="210dd-137">Идентификатор контекста, используемый драйвером для последующей передачи данных.</span><span class="sxs-lookup"><span data-stu-id="210dd-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="210dd-138">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="210dd-138">Calling Methods</span></span>

<span data-ttu-id="210dd-139">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="210dd-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="210dd-140">Требования</span><span class="sxs-lookup"><span data-stu-id="210dd-140">Requirements</span></span>



| <span data-ttu-id="210dd-141">Требование</span><span class="sxs-lookup"><span data-stu-id="210dd-141">Requirement</span></span> | <span data-ttu-id="210dd-142">Значение</span><span class="sxs-lookup"><span data-stu-id="210dd-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="210dd-143">Header</span><span class="sxs-lookup"><span data-stu-id="210dd-143">Header</span></span><br/> | <dl> <span data-ttu-id="210dd-144"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="210dd-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="210dd-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="210dd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210dd-146">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="210dd-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




