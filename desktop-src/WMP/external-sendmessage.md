---
title: External. sendMessage, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод sendMessage отправляет сообщение подключаемому модулю Интернет-магазина.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- sendMessage, метод Windows Media Player
- sendMessage метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695063"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="5ecf5-108">External. sendMessage, метод</span><span class="sxs-lookup"><span data-stu-id="5ecf5-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="5ecf5-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5ecf5-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5ecf5-111">Метод **SendMessage** отправляет сообщение подключаемому модулю Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecf5-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ecf5-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="5ecf5-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ecf5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ecf5-114">*Сообщение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ecf5-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecf5-115">**Строка** , содержащая сообщение.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="5ecf5-116">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ecf5-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecf5-117">**Строка** , содержащая параметры, связанные с сообщением.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ecf5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ecf5-118">Return value</span></span>

<span data-ttu-id="5ecf5-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ecf5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ecf5-120">Remarks</span></span>

<span data-ttu-id="5ecf5-121">Сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-121">The message is sent asynchronously.</span></span> <span data-ttu-id="5ecf5-122">Это значит, что этот метод возвращает значение немедленно, а не ожидает обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="5ecf5-123">Когда подключаемый модуль заканчивает обработку сообщения, он вызывает метод [ивмпконтентпартнеркаллбакк:: сендмессажекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , который, в свою очередь, вызывает обработчик событий [онсендмессажекомплете](external-onsendmessagecomplete-event.md) в скрипте.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecf5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5ecf5-124">Requirements</span></span>



| <span data-ttu-id="5ecf5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5ecf5-125">Requirement</span></span> | <span data-ttu-id="5ecf5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5ecf5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecf5-127">Версия</span><span class="sxs-lookup"><span data-stu-id="5ecf5-127">Version</span></span><br/> | <span data-ttu-id="5ecf5-128">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="5ecf5-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="5ecf5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecf5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ecf5-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecf5-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecf5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ecf5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecf5-132">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="5ecf5-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5ecf5-133">**External. Онсендмессажекомплете**</span><span class="sxs-lookup"><span data-stu-id="5ecf5-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="5ecf5-134">**Ивмпконтентпартнер:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5ecf5-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="5ecf5-135">**Ивмпконтентпартнеркаллбакк:: Сендмессажекомплете**</span><span class="sxs-lookup"><span data-stu-id="5ecf5-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





