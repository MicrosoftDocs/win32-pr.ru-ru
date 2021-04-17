---
description: Команда WPD \_ , \_ \_ \_ полученная при \_ получении \_ описания расширения поставщика \_ , получает строку описания поставщика-расширения. Эта строка определяется набором данных DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Команда WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708380"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="284e4-104">Команда WPD команда для \_ \_ \_ \_ получения \_ расширения поставщику \_ расширений \_ MTP</span><span class="sxs-lookup"><span data-stu-id="284e4-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="284e4-105">Команда **WPD \_ , \_ \_ \_ полученная при \_ получении \_ \_ описания расширения поставщика** , получает строку описания поставщика-расширения.</span><span class="sxs-lookup"><span data-stu-id="284e4-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="284e4-106">Эта строка определяется набором данных **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="284e4-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="284e4-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="284e4-107">Command category</span></span>

<span data-ttu-id="284e4-108">**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="284e4-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="284e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="284e4-109">Parameters</span></span>

<span data-ttu-id="284e4-110">У этой команды нет параметров.</span><span class="sxs-lookup"><span data-stu-id="284e4-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="284e4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="284e4-111">Return Value</span></span>

<span data-ttu-id="284e4-112">Драйвер возвращает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="284e4-112">The driver returns the following results.</span></span>



| <span data-ttu-id="284e4-113">Результат</span><span class="sxs-lookup"><span data-stu-id="284e4-113">Result</span></span>                                                      | <span data-ttu-id="284e4-114">VarType</span><span class="sxs-lookup"><span data-stu-id="284e4-114">VarType</span></span>    | <span data-ttu-id="284e4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="284e4-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="284e4-116">**\_Описание свойства WPD для \_ \_ \_ \_ расширения поставщика \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="284e4-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="284e4-117">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="284e4-117">VT\_LPWSTR</span></span> | <span data-ttu-id="284e4-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="284e4-118">Required.</span></span> <span data-ttu-id="284e4-119">Указывает строку описания поставщика-расширения.</span><span class="sxs-lookup"><span data-stu-id="284e4-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="284e4-120">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="284e4-120">Calling Methods</span></span>

<span data-ttu-id="284e4-121">Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="284e4-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="284e4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="284e4-122">Requirements</span></span>



| <span data-ttu-id="284e4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="284e4-123">Requirement</span></span> | <span data-ttu-id="284e4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="284e4-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="284e4-125">Header</span><span class="sxs-lookup"><span data-stu-id="284e4-125">Header</span></span><br/> | <dl> <span data-ttu-id="284e4-126"><dt>Впдмтпекстенсионс. h</dt></span><span class="sxs-lookup"><span data-stu-id="284e4-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284e4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="284e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284e4-128">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="284e4-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




