---
description: Команда WPD с командой \_ \_ MTP \_ \_ Get \_ Supported \_ Vendor \_ код отправляет блок команд MTP. Отсутствует последующий этап данных, связанный с этой командой.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Команда WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708382"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="bc797-104">Команда WPD с командой \_ \_ MTP \_ \_ Get \_ поддерживаемые \_ поставщики \_ кодов операций</span><span class="sxs-lookup"><span data-stu-id="bc797-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="bc797-105">Команда **WPD с командой \_ \_ MTP \_ \_ Get \_ Supported \_ Vendor \_ код** отправляет блок команд MTP.</span><span class="sxs-lookup"><span data-stu-id="bc797-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="bc797-106">Отсутствует последующий этап данных, связанный с этой командой.</span><span class="sxs-lookup"><span data-stu-id="bc797-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="bc797-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="bc797-107">Command category</span></span>

<span data-ttu-id="bc797-108">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc797-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="bc797-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc797-109">Parameters</span></span>

<span data-ttu-id="bc797-110">У этой команды нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bc797-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc797-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc797-111">Return Value</span></span>

<span data-ttu-id="bc797-112">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="bc797-112">The driver returns the following results.</span></span>



| <span data-ttu-id="bc797-113">Результат</span><span class="sxs-lookup"><span data-stu-id="bc797-113">Result</span></span>                                                | <span data-ttu-id="bc797-114">VarType</span><span class="sxs-lookup"><span data-stu-id="bc797-114">VarType</span></span> | <span data-ttu-id="bc797-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bc797-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc797-116">**\_коды операций для свойства WPD \_ MTP \_ ext \_ поставщика \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc797-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="bc797-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bc797-117">VT\_UI4</span></span> | <span data-ttu-id="bc797-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="bc797-118">Required.</span></span> <span data-ttu-id="bc797-119">**Ипортабледевицепропвариантколлектион** , содержащий все коды расширенных операций, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bc797-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="bc797-120">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="bc797-120">Calling Methods</span></span>

<span data-ttu-id="bc797-121">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="bc797-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc797-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bc797-122">Requirements</span></span>



| <span data-ttu-id="bc797-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bc797-123">Requirement</span></span> | <span data-ttu-id="bc797-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bc797-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc797-125">Header</span><span class="sxs-lookup"><span data-stu-id="bc797-125">Header</span></span><br/> | <dl> <span data-ttu-id="bc797-126"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc797-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc797-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc797-128">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="bc797-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




