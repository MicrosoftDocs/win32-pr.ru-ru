---
description: Уведомляет о преобразовании Media Foundation (MFT), которое будет обработано первым образцом.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080437"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="e8177-103">\_ \_ уведомление о \_ начале \_ потока в \_ сообщении MFT</span><span class="sxs-lookup"><span data-stu-id="e8177-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="e8177-104">Уведомляет о преобразовании Media Foundation (MFT), которое будет обработано первым образцом.</span><span class="sxs-lookup"><span data-stu-id="e8177-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="e8177-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="e8177-105">Message Parameter</span></span>

<span data-ttu-id="e8177-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8177-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8177-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="e8177-107">Remarks</span></span>

<span data-ttu-id="e8177-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="e8177-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="e8177-109">Для синхронных МФТС необязательно отправить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8177-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="e8177-110">Для асинхронного МФТС клиент должен отправить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8177-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="e8177-111">Реализация</span><span class="sxs-lookup"><span data-stu-id="e8177-111">Implementation</span></span>

<span data-ttu-id="e8177-112">Синхронная MFT не требуется для ответа на сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8177-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="e8177-113">Асинхронная Таблица MFT должна реализовывать это сообщение, как описано в статье [асинхронный МФТС](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="e8177-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8177-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e8177-114">Requirements</span></span>



| <span data-ttu-id="e8177-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e8177-115">Requirement</span></span> | <span data-ttu-id="e8177-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e8177-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8177-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8177-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8177-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8177-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8177-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8177-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8177-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8177-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e8177-121">Header</span><span class="sxs-lookup"><span data-stu-id="e8177-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8177-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8177-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8177-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8177-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8177-124">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="e8177-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




