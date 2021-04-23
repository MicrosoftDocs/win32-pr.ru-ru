---
description: Команда WPD команды " \_ \_ MTP \_ ext \_ Read \_ Data" извлекает данные с устройства после выполнения команды \_ WPD \_ MTP \_ ext \_ Execute \_ \_ с командой \_ Data \_ to \_ Read.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Команда WPD_COMMAND_MTP_EXT_READ_DATA (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708379"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="9e3ea-103">Команда WPD, \_ \_ \_ команда MTP ext \_ Read \_ Data</span><span class="sxs-lookup"><span data-stu-id="9e3ea-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="9e3ea-104">Команда **WPD команды " \_ \_ MTP \_ ext \_ Read \_ data** " извлекает данные с устройства после выполнения **команды \_ WPD \_ MTP \_ ext \_ Execute \_ \_ с командой \_ Data \_ to \_ Read** .</span><span class="sxs-lookup"><span data-stu-id="9e3ea-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="9e3ea-105">Категория команды</span><span class="sxs-lookup"><span data-stu-id="9e3ea-105">Command category</span></span>

<span data-ttu-id="9e3ea-106">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="9e3ea-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e3ea-107">Parameters</span></span>

<span data-ttu-id="9e3ea-108">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="9e3ea-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="9e3ea-109">Parameter</span></span>                                                   | <span data-ttu-id="9e3ea-110">VarType</span><span class="sxs-lookup"><span data-stu-id="9e3ea-110">VarType</span></span>             | <span data-ttu-id="9e3ea-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9e3ea-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3ea-112">**\_свойство WPD \_ для \_ \_ контекста перемещения \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="9e3ea-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9e3ea-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="9e3ea-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-114">Required.</span></span> <span data-ttu-id="9e3ea-115">Определяет контекст, возвращенный предыдущим вызовом к устройству.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="9e3ea-116">**\_свойство WPD \_ . \_ \_ \_ число \_ байтов \_ для чтения (в байтах \_ ) MTP**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="9e3ea-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9e3ea-117">VT\_UI4</span></span>             | <span data-ttu-id="9e3ea-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-118">Required.</span></span> <span data-ttu-id="9e3ea-119">Указывает число байтов для чтения.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="9e3ea-120">**Свойство WPD. Дополнительные \_ \_ данные о \_ \_ передаваемых \_ данных MTP**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="9e3ea-121">VT \_ вектор \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="9e3ea-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="9e3ea-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-122">Required.</span></span> <span data-ttu-id="9e3ea-123">Определяет буфер, в который копируются данные устройства.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="9e3ea-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e3ea-124">Return Value</span></span>

<span data-ttu-id="9e3ea-125">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-125">The driver returns the following results.</span></span>



| <span data-ttu-id="9e3ea-126">Результат</span><span class="sxs-lookup"><span data-stu-id="9e3ea-126">Result</span></span>                                                  | <span data-ttu-id="9e3ea-127">VarType</span><span class="sxs-lookup"><span data-stu-id="9e3ea-127">VarType</span></span>             | <span data-ttu-id="9e3ea-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9e3ea-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9e3ea-129">**\_ \_ \_ \_ \_ число \_ \_ прочитанных байт в свойстве WPD MTP**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="9e3ea-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9e3ea-130">VT\_UI4</span></span>             | <span data-ttu-id="9e3ea-131">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-131">Required.</span></span> <span data-ttu-id="9e3ea-132">Указывает число байтов, полученных от устройства.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="9e3ea-133">**Свойство WPD. Дополнительные \_ \_ данные о \_ \_ передаваемых \_ данных MTP**</span><span class="sxs-lookup"><span data-stu-id="9e3ea-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="9e3ea-134">VT \_ вектор \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="9e3ea-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="9e3ea-135">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-135">Required.</span></span> <span data-ttu-id="9e3ea-136">Буфер, содержащий данные устройства.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="9e3ea-137">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="9e3ea-137">Calling Methods</span></span>

<span data-ttu-id="9e3ea-138">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="9e3ea-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3ea-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9e3ea-139">Requirements</span></span>



| <span data-ttu-id="9e3ea-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9e3ea-140">Requirement</span></span> | <span data-ttu-id="9e3ea-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9e3ea-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3ea-142">Header</span><span class="sxs-lookup"><span data-stu-id="9e3ea-142">Header</span></span><br/> | <dl> <span data-ttu-id="9e3ea-143"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e3ea-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3ea-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e3ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3ea-145">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="9e3ea-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




