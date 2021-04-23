---
description: '\_ \_ Событие КОДЕКАПИ события EC отправляется кодировщиком для сигнализации о событии кодирования. Клиент регистрируется для события кодировщика путем вызова метода Икодекапи:: Регистерфоревент.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675571"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="d984e-104">\_событие EC кодекапи \_</span><span class="sxs-lookup"><span data-stu-id="d984e-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="d984e-105">\_ \_ Событие КОДЕКАПИ события EC отправляется кодировщиком для сигнализации о событии кодирования.</span><span class="sxs-lookup"><span data-stu-id="d984e-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="d984e-106">Клиент регистрируется для события кодировщика путем вызова метода [**икодекапи:: регистерфоревент**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="d984e-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="d984e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d984e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d984e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d984e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d984e-109">Данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="d984e-109">User data.</span></span> <span data-ttu-id="d984e-110">Значением этого параметра является указатель, указанный вызывающим объектом в параметре *UserData* метода [**регистерфоревент**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="d984e-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="d984e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d984e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d984e-112">Указатель на данные события.</span><span class="sxs-lookup"><span data-stu-id="d984e-112">Pointer to the event data.</span></span> <span data-ttu-id="d984e-113">Эти данные выделяются кодировщиком и должны быть освобождены приложением с помощью функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="d984e-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="d984e-114">Блок данных начинается со структуры [**кодекапиевентдата**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Приведите параметр *lParam2* к указателю на эту структуру.</span><span class="sxs-lookup"><span data-stu-id="d984e-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d984e-115">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d984e-115">Default Action</span></span>

<span data-ttu-id="d984e-116">Нет действия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d984e-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="d984e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d984e-117">Requirements</span></span>



| <span data-ttu-id="d984e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d984e-118">Requirement</span></span> | <span data-ttu-id="d984e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d984e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d984e-120">Header</span><span class="sxs-lookup"><span data-stu-id="d984e-120">Header</span></span><br/> | <dl> <span data-ttu-id="d984e-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d984e-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d984e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d984e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d984e-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="d984e-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d984e-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d984e-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




