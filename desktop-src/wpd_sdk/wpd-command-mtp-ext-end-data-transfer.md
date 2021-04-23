---
description: Команда WPD \_ , \_ \_ \_ завершающая завершение данных команды MTP, \_ \_ завершает обмен данными и считывает ответ от устройства.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Команда WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708458"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="61fba-103">Команда WPD Command \_ \_ MTP \_ \_ закончить \_ \_ Перенос данных</span><span class="sxs-lookup"><span data-stu-id="61fba-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="61fba-104">Команда **WPD \_ , \_ \_ \_ завершающая завершение \_ данных \_ команды MTP** , завершает обмен данными и считывает ответ от устройства.</span><span class="sxs-lookup"><span data-stu-id="61fba-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="61fba-105">Эта отправка инициируется командой " [**WPD" \_ ( \_ MTP \_ ext \_ EXECUTE) с командой " \_ \_ \_ данные \_ для \_ чтения**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) " или [**командой WPD команды "MTP" выполнить команду \_ \_ \_ \_ \_ \_ с \_ данными \_ для \_ записи**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) .</span><span class="sxs-lookup"><span data-stu-id="61fba-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="61fba-106">Категория команды</span><span class="sxs-lookup"><span data-stu-id="61fba-106">Command category</span></span>

<span data-ttu-id="61fba-107">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61fba-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="61fba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61fba-108">Parameters</span></span>

<span data-ttu-id="61fba-109">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="61fba-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="61fba-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="61fba-110">Parameter</span></span>                                      | <span data-ttu-id="61fba-111">VarType</span><span class="sxs-lookup"><span data-stu-id="61fba-111">VarType</span></span>    | <span data-ttu-id="61fba-112">Описание</span><span class="sxs-lookup"><span data-stu-id="61fba-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="61fba-113">**\_свойство WPD \_ для \_ \_ контекста перемещения \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="61fba-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="61fba-114">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="61fba-114">VT\_LPWSTR</span></span> | <span data-ttu-id="61fba-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="61fba-115">Required.</span></span> <span data-ttu-id="61fba-116">Определяет контекст, возвращаемый предыдущим вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="61fba-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="61fba-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61fba-117">Return Value</span></span>

<span data-ttu-id="61fba-118">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="61fba-118">The driver returns the following results.</span></span>



| <span data-ttu-id="61fba-119">Результат</span><span class="sxs-lookup"><span data-stu-id="61fba-119">Result</span></span>                                        | <span data-ttu-id="61fba-120">VarType</span><span class="sxs-lookup"><span data-stu-id="61fba-120">VarType</span></span> | <span data-ttu-id="61fba-121">Описание</span><span class="sxs-lookup"><span data-stu-id="61fba-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fba-122">**\_свойство WPD \_ , \_ \_ код ответа \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="61fba-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="61fba-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="61fba-123">VT\_UI4</span></span> | <span data-ttu-id="61fba-124">Обязательный. код ответа на код операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="61fba-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="61fba-125">**\_Свойства WPD \_ \_ \_ параметры ответа MTP \_ ext**</span><span class="sxs-lookup"><span data-stu-id="61fba-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="61fba-126">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="61fba-126">VT\_UI4</span></span> | <span data-ttu-id="61fba-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="61fba-127">Optional.</span></span> <span data-ttu-id="61fba-128">Коллекция **ипортабледевицепропвариантколлектион** , которая определяет параметры ответа.</span><span class="sxs-lookup"><span data-stu-id="61fba-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="61fba-129">Эта коллекция может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="61fba-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="61fba-130">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="61fba-130">Calling Methods</span></span>

<span data-ttu-id="61fba-131">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="61fba-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="61fba-132">Требования</span><span class="sxs-lookup"><span data-stu-id="61fba-132">Requirements</span></span>



| <span data-ttu-id="61fba-133">Требование</span><span class="sxs-lookup"><span data-stu-id="61fba-133">Requirement</span></span> | <span data-ttu-id="61fba-134">Значение</span><span class="sxs-lookup"><span data-stu-id="61fba-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fba-135">Header</span><span class="sxs-lookup"><span data-stu-id="61fba-135">Header</span></span><br/> | <dl> <span data-ttu-id="61fba-136"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="61fba-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fba-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61fba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fba-138">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="61fba-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

