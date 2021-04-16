---
description: Команда WPD \_ , \_ \_ выполняемая командой MTP \_ без команды \_ \_ \_ \_ этапа данных, отправляет блок команд MTP. Отсутствует последующий этап данных, связанный с этой командой.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Команда WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708383"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="afe72-104">Команда \_ WPD \_ MTP \_ команда \_ Execute \_ \_ без \_ \_ команды этапа данных</span><span class="sxs-lookup"><span data-stu-id="afe72-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="afe72-105">Команда **WPD \_ , \_ \_ выполняемая командой MTP \_ без команды \_ \_ \_ \_ этапа данных** , отправляет блок команд MTP.</span><span class="sxs-lookup"><span data-stu-id="afe72-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="afe72-106">Отсутствует последующий этап данных, связанный с этой командой.</span><span class="sxs-lookup"><span data-stu-id="afe72-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="afe72-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="afe72-107">Command category</span></span>

<span data-ttu-id="afe72-108">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="afe72-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="afe72-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="afe72-109">Parameters</span></span>

<span data-ttu-id="afe72-110">Драйверу требуются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="afe72-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="afe72-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="afe72-111">Parameter</span></span>                                      | <span data-ttu-id="afe72-112">VarType</span><span class="sxs-lookup"><span data-stu-id="afe72-112">VarType</span></span> | <span data-ttu-id="afe72-113">Описание</span><span class="sxs-lookup"><span data-stu-id="afe72-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe72-114">**\_свойство WPD \_ \_ \_ код операции MTP \_**</span><span class="sxs-lookup"><span data-stu-id="afe72-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="afe72-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="afe72-115">VT\_UI4</span></span> | <span data-ttu-id="afe72-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="afe72-116">Required.</span></span> <span data-ttu-id="afe72-117">Идентифицирует код операции, расширенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="afe72-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="afe72-118">**\_Свойства WPD \_ для \_ \_ параметров операции ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="afe72-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="afe72-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="afe72-119">VT\_UI4</span></span> | <span data-ttu-id="afe72-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="afe72-120">Required.</span></span> <span data-ttu-id="afe72-121">Объект **ипортабледевицепропвариантколлектион**, который определяет обязательные параметры для кода операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="afe72-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="afe72-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afe72-122">Return Value</span></span>

<span data-ttu-id="afe72-123">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="afe72-123">The driver returns the following results.</span></span>



| <span data-ttu-id="afe72-124">Результат</span><span class="sxs-lookup"><span data-stu-id="afe72-124">Result</span></span>                                        | <span data-ttu-id="afe72-125">VarType</span><span class="sxs-lookup"><span data-stu-id="afe72-125">VarType</span></span> | <span data-ttu-id="afe72-126">Описание</span><span class="sxs-lookup"><span data-stu-id="afe72-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe72-127">**\_свойство WPD \_ , \_ \_ код ответа \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="afe72-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="afe72-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="afe72-128">VT\_UI4</span></span> | <span data-ttu-id="afe72-129">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="afe72-129">Required.</span></span> <span data-ttu-id="afe72-130">Код ответа на код операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="afe72-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="afe72-131">**\_Свойства WPD \_ \_ \_ параметры ответа MTP \_ ext**</span><span class="sxs-lookup"><span data-stu-id="afe72-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="afe72-132">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="afe72-132">VT\_UI4</span></span> | <span data-ttu-id="afe72-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="afe72-133">Optional.</span></span> <span data-ttu-id="afe72-134">Объект **ипортабледевицепропвариантколлектион** , определяющий параметры ответа.</span><span class="sxs-lookup"><span data-stu-id="afe72-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="afe72-135">Эта коллекция может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="afe72-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="afe72-136">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="afe72-136">Calling Methods</span></span>

<span data-ttu-id="afe72-137">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="afe72-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="afe72-138">Требования</span><span class="sxs-lookup"><span data-stu-id="afe72-138">Requirements</span></span>



| <span data-ttu-id="afe72-139">Требование</span><span class="sxs-lookup"><span data-stu-id="afe72-139">Requirement</span></span> | <span data-ttu-id="afe72-140">Значение</span><span class="sxs-lookup"><span data-stu-id="afe72-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe72-141">Header</span><span class="sxs-lookup"><span data-stu-id="afe72-141">Header</span></span><br/> | <dl> <span data-ttu-id="afe72-142"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="afe72-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe72-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afe72-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe72-144">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="afe72-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




