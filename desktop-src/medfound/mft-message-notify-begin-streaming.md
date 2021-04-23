---
description: Уведомляет Media Foundation преобразование (MFT), которое начинается потоковая передача.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263514"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="e4b53-103">\_ \_ уведомление о \_ начале \_ ПОТОКовой передачи сообщения MFT</span><span class="sxs-lookup"><span data-stu-id="e4b53-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="e4b53-104">Уведомляет Media Foundation преобразование (MFT), которое начинается потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="e4b53-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="e4b53-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="e4b53-105">Message Parameter</span></span>

<span data-ttu-id="e4b53-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="e4b53-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b53-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="e4b53-107">Remarks</span></span>

<span data-ttu-id="e4b53-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="e4b53-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="e4b53-109">Клиенту не требуется отсылать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e4b53-109">The client is not required to send this message.</span></span> <span data-ttu-id="e4b53-110">Если клиент отправляет это сообщение, он должен сделать это после установки всех типов носителей в MFT и перед вызовом метода [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="e4b53-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="e4b53-111">MFT может ответить путем выделения буферов или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4b53-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="e4b53-112">Если клиент не отправляет это сообщение, MFT выделяет ресурсы при первом вызове **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="e4b53-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="e4b53-113">Поэтому отправка этого сообщения может уменьшить начальную задержку при запуске потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e4b53-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="e4b53-114">Реализация</span><span class="sxs-lookup"><span data-stu-id="e4b53-114">Implementation</span></span>

<span data-ttu-id="e4b53-115">MFT не требуется для ответа на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e4b53-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b53-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b53-116">Requirements</span></span>



| <span data-ttu-id="e4b53-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b53-117">Requirement</span></span> | <span data-ttu-id="e4b53-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b53-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b53-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b53-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4b53-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e4b53-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b53-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4b53-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e4b53-123">Header</span><span class="sxs-lookup"><span data-stu-id="e4b53-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b53-124"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b53-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b53-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b53-126">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="e4b53-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




