---
description: Портативные устройства Windows поддерживают следующие свойства SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Свойства SMS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717861"
---
# <a name="sms-properties"></a><span data-ttu-id="b8e7a-103">Свойства SMS</span><span class="sxs-lookup"><span data-stu-id="b8e7a-103">SMS Properties</span></span>

<span data-ttu-id="b8e7a-104">Портативные устройства Windows поддерживают следующие свойства SMS.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="b8e7a-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="b8e7a-105">Property</span></span>                   | <span data-ttu-id="b8e7a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="b8e7a-106">VarType</span></span>        | <span data-ttu-id="b8e7a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b8e7a-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e7a-108">**\_кодирование SMS \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="b8e7a-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b8e7a-110">Значение, указывающее, как драйвер будет кодировать текстовое сообщение, отправленное клиентом.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="b8e7a-111">Это свойство доступно только для чтения. Клиент не может указать тип кодировки, который устройство использует для отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="b8e7a-112">Эти значения дублируют перечислимые значения [**\_ \_ \_ типов кодирования типа WPD SMS**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="b8e7a-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="b8e7a-113">**\_ \_ Максимальное количество полезных данных по SMS для сервера WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="b8e7a-114">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-114">**VT\_UI4**</span></span>    | <span data-ttu-id="b8e7a-115">Максимальное число байтов, которое может содержаться в сообщении.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="b8e7a-116">**\_поставщик SMS для WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="b8e7a-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b8e7a-118">Имя поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b8e7a-119">**\_время ожидания SMS-сервера (WPD) \_**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="b8e7a-120">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-120">**VT\_UI4**</span></span>    | <span data-ttu-id="b8e7a-121">Количество миллисекунд, пока не будет возвращено время ожидания.</span><span class="sxs-lookup"><span data-stu-id="b8e7a-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="b8e7a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b8e7a-122">Requirements</span></span>



| <span data-ttu-id="b8e7a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b8e7a-123">Requirement</span></span> | <span data-ttu-id="b8e7a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b8e7a-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e7a-125">Header</span><span class="sxs-lookup"><span data-stu-id="b8e7a-125">Header</span></span><br/> | <dl> <span data-ttu-id="b8e7a-126"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e7a-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e7a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8e7a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e7a-128">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="b8e7a-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




