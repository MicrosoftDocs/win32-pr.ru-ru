---
description: Команда WPD \_ \_ MTP \_ ext \_ Write \_ передает данные на устройство после выполнения команды WPD \_ \_ MTP \_ \_ EXECUTE с командой \_ \_ \_ Data \_ to \_ Write.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Команда WPD_COMMAND_MTP_EXT_WRITE_DATA (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708378"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="40e28-103">Команда WPD команды \_ \_ MTP \_ ext \_ Write \_ Data</span><span class="sxs-lookup"><span data-stu-id="40e28-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="40e28-104">Команда **WPD \_ \_ MTP \_ ext \_ Write \_** передает данные на устройство после выполнения команды **WPD \_ \_ MTP \_ \_ EXECUTE с командой \_ \_ \_ Data \_ to \_ Write** .</span><span class="sxs-lookup"><span data-stu-id="40e28-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="40e28-105">Категория команды</span><span class="sxs-lookup"><span data-stu-id="40e28-105">Command category</span></span>

<span data-ttu-id="40e28-106">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40e28-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="40e28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40e28-107">Parameters</span></span>

<span data-ttu-id="40e28-108">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="40e28-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="40e28-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="40e28-109">Parameter</span></span>                                                    | <span data-ttu-id="40e28-110">VarType</span><span class="sxs-lookup"><span data-stu-id="40e28-110">VarType</span></span>             | <span data-ttu-id="40e28-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40e28-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40e28-112">**\_свойство WPD \_ для \_ \_ контекста перемещения \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="40e28-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="40e28-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="40e28-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="40e28-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40e28-114">Required.</span></span> <span data-ttu-id="40e28-115">Определяет контекст, возвращенный предыдущим вызовом к устройству.</span><span class="sxs-lookup"><span data-stu-id="40e28-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="40e28-116">**\_свойство WPD \_ . \_ \_ \_ число \_ байт \_ для \_ записи**</span><span class="sxs-lookup"><span data-stu-id="40e28-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="40e28-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="40e28-117">VT\_UI4</span></span>             | <span data-ttu-id="40e28-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40e28-118">Required.</span></span> <span data-ttu-id="40e28-119">Указывает число байтов для записи.</span><span class="sxs-lookup"><span data-stu-id="40e28-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="40e28-120">**Свойство WPD. Дополнительные \_ \_ данные о \_ \_ передаваемых \_ данных MTP**</span><span class="sxs-lookup"><span data-stu-id="40e28-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="40e28-121">VT \_ вектор \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="40e28-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="40e28-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40e28-122">Required.</span></span> <span data-ttu-id="40e28-123">Определяет буфер, в который копируются данные устройства.</span><span class="sxs-lookup"><span data-stu-id="40e28-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="40e28-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40e28-124">Return Value</span></span>

<span data-ttu-id="40e28-125">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="40e28-125">The driver returns the following results.</span></span>



| <span data-ttu-id="40e28-126">Результат</span><span class="sxs-lookup"><span data-stu-id="40e28-126">Result</span></span>                                                     | <span data-ttu-id="40e28-127">VarType</span><span class="sxs-lookup"><span data-stu-id="40e28-127">VarType</span></span> | <span data-ttu-id="40e28-128">Описание</span><span class="sxs-lookup"><span data-stu-id="40e28-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="40e28-129">**\_ \_ \_ \_ \_ число \_ \_ записанных байт для свойства WPD MTP**</span><span class="sxs-lookup"><span data-stu-id="40e28-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="40e28-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="40e28-130">VT\_UI4</span></span> | <span data-ttu-id="40e28-131">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40e28-131">Required.</span></span> <span data-ttu-id="40e28-132">Указывает число байтов, отправленных на устройство.</span><span class="sxs-lookup"><span data-stu-id="40e28-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="40e28-133">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="40e28-133">Calling Methods</span></span>

<span data-ttu-id="40e28-134">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="40e28-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="40e28-135">Требования</span><span class="sxs-lookup"><span data-stu-id="40e28-135">Requirements</span></span>



| <span data-ttu-id="40e28-136">Требование</span><span class="sxs-lookup"><span data-stu-id="40e28-136">Requirement</span></span> | <span data-ttu-id="40e28-137">Значение</span><span class="sxs-lookup"><span data-stu-id="40e28-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e28-138">Header</span><span class="sxs-lookup"><span data-stu-id="40e28-138">Header</span></span><br/> | <dl> <span data-ttu-id="40e28-139"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="40e28-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e28-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40e28-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e28-141">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="40e28-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




