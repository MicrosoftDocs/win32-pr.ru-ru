---
description: Запрашивает преобразование Media Foundation (MFT) в эту потоковую передачу.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543911"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="ef55b-103">\_ \_ уведомление о \_ завершении \_ ПОТОКовой передачи сообщения MFT</span><span class="sxs-lookup"><span data-stu-id="ef55b-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="ef55b-104">Запрашивает преобразование Media Foundation (MFT) в эту потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="ef55b-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="ef55b-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="ef55b-105">Message Parameter</span></span>

<span data-ttu-id="ef55b-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="ef55b-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef55b-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef55b-107">Remarks</span></span>

<span data-ttu-id="ef55b-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="ef55b-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="ef55b-109">Клиенту не требуется отправлять это сообщение, даже если клиент ранее отправил сообщение **MFT с \_ \_ уведомлением о \_ начале \_ потоковой передачи** .</span><span class="sxs-lookup"><span data-stu-id="ef55b-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="ef55b-110">Реализация</span><span class="sxs-lookup"><span data-stu-id="ef55b-110">Implementation</span></span>

<span data-ttu-id="ef55b-111">MFT может ответить на это сообщение, освобождая буферы и другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ef55b-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="ef55b-112">Таблица MFT не очищает входные данные или не сбрасывает типы носителей в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ef55b-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="ef55b-113">MFT не требуется для ответа на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ef55b-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef55b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ef55b-114">Requirements</span></span>



| <span data-ttu-id="ef55b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ef55b-115">Requirement</span></span> | <span data-ttu-id="ef55b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ef55b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef55b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef55b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef55b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef55b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef55b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef55b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef55b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef55b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef55b-121">Header</span><span class="sxs-lookup"><span data-stu-id="ef55b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef55b-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef55b-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef55b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef55b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef55b-124">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="ef55b-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




