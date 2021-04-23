---
description: Команда WPD \_ \_ Common \_ Reset \_ Device сбрасывает устройство. Это не означает переформатирование. Он эквивалентен выключению и повторному включению устройства.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Команда WPD_COMMAND_COMMON_RESET_DEVICE (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708604"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="6415c-104">\_Команда WPD \_ Common \_ rereset \_ Device</span><span class="sxs-lookup"><span data-stu-id="6415c-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="6415c-105">Команда **WPD \_ \_ Common \_ Reset \_ Device** сбрасывает устройство.</span><span class="sxs-lookup"><span data-stu-id="6415c-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="6415c-106">Это не означает переформатирование. Он эквивалентен выключению и повторному включению устройства.</span><span class="sxs-lookup"><span data-stu-id="6415c-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="6415c-107">Категория команды</span><span class="sxs-lookup"><span data-stu-id="6415c-107">Command category</span></span>

<span data-ttu-id="6415c-108">**\_Категория WPD \_ Common**</span><span class="sxs-lookup"><span data-stu-id="6415c-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="6415c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6415c-109">Parameters</span></span>

<span data-ttu-id="6415c-110">У этой команды нет параметров.</span><span class="sxs-lookup"><span data-stu-id="6415c-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6415c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6415c-111">Return Value</span></span>

<span data-ttu-id="6415c-112">Драйвер должен вернуть следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="6415c-112">The driver should return the following results.</span></span>



| <span data-ttu-id="6415c-113">Результат</span><span class="sxs-lookup"><span data-stu-id="6415c-113">Result</span></span>                                         | <span data-ttu-id="6415c-114">VarType</span><span class="sxs-lookup"><span data-stu-id="6415c-114">VarType</span></span>   | <span data-ttu-id="6415c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6415c-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6415c-116">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6415c-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="6415c-117">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="6415c-117">VT\_ERROR</span></span> | <span data-ttu-id="6415c-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6415c-118">Required.</span></span> <span data-ttu-id="6415c-119">**Значение HRESULT** , указывающее на успешное выполнение или неудачу выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="6415c-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="6415c-120">Если вызывающий объект делает недопустимый запрос, драйвер должен вернуть **значение HRESULT \_ из \_ Win32 (ошибка \_ не \_ поддерживается)** и не требуется возвращать какие-либо другие результирующие значения.</span><span class="sxs-lookup"><span data-stu-id="6415c-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="6415c-121">Коды ошибок включают в себя [коды ошибок переносных устройств Windows](error-constants.md) или любые другие соответствующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="6415c-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="6415c-122">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="6415c-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="6415c-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6415c-123">VT\_UI4</span></span>   | <span data-ttu-id="6415c-124">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6415c-124">Optional.</span></span> <span data-ttu-id="6415c-125">Код ошибки, относящийся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="6415c-125">A driver-specific error code.</span></span> <span data-ttu-id="6415c-126">Обычно это используется только для тестирования драйверов или, если все драйверы, устройства и клиенты разработаны вместе.</span><span class="sxs-lookup"><span data-stu-id="6415c-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="6415c-127">Вызов методов</span><span class="sxs-lookup"><span data-stu-id="6415c-127">Calling Methods</span></span>

<span data-ttu-id="6415c-128">Может вызываться напрямую только с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="6415c-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="6415c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="6415c-129">Requirements</span></span>



| <span data-ttu-id="6415c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="6415c-130">Requirement</span></span> | <span data-ttu-id="6415c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6415c-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6415c-132">Header</span><span class="sxs-lookup"><span data-stu-id="6415c-132">Header</span></span><br/> | <dl> <span data-ttu-id="6415c-133"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="6415c-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6415c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6415c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6415c-135">**Команды**</span><span class="sxs-lookup"><span data-stu-id="6415c-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




