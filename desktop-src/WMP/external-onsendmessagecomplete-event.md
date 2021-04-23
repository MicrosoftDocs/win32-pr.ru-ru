---
title: Внешнее событие Онсендмессажекомплете
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Онсендмессажекомплете
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Проигрыватель Windows Media для события external. Онсендмессажекомплете
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694495"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="36c46-105">Внешнее событие Онсендмессажекомплете</span><span class="sxs-lookup"><span data-stu-id="36c46-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="36c46-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="36c46-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="36c46-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="36c46-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="36c46-108">Событие **онсендмессажекомплете** возникает, когда Интернет-магазин завершил обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="36c46-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="36c46-109">Сценарий на странице обнаружения ранее отправил сообщение путем вызова метода [External. SendMessage](external-sendmessage.md).</span><span class="sxs-lookup"><span data-stu-id="36c46-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="36c46-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="36c46-110">Possible Values</span></span>

<span data-ttu-id="36c46-111">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="36c46-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="36c46-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="36c46-112">Parameters</span></span>

<span data-ttu-id="36c46-113">Функция, обрабатывающая это событие, имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="36c46-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="36c46-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Об*</span><span class="sxs-lookup"><span data-stu-id="36c46-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="36c46-115">Та же строка, которая была передана в параметре **MSG** для **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="36c46-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="36c46-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Байт*</span><span class="sxs-lookup"><span data-stu-id="36c46-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="36c46-117">Та же строка, которая была передана в параметре **param** для **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="36c46-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="36c46-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Результат*</span><span class="sxs-lookup"><span data-stu-id="36c46-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="36c46-119">**Строка** , содержащая результат обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="36c46-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="36c46-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="36c46-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36c46-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36c46-121">Remarks</span></span>

<span data-ttu-id="36c46-122">Метод **SendMessage** вызывает [Ивмпконтентпартнер:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), который возвращает асинхронно.</span><span class="sxs-lookup"><span data-stu-id="36c46-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="36c46-123">То есть он возвращается до того, как Интернет-магазин завершит обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="36c46-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="36c46-124">Когда Интернет-магазин заканчивает обработку сообщения, он вызывает [ивмпконтентпартнеркаллбакк:: сендмессажекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), который, в свою очередь, вызывает обработчик событий **онсендмессажекомплете** в скрипте.</span><span class="sxs-lookup"><span data-stu-id="36c46-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="36c46-125">Когда Интернет-магазин вызывает **ивмпконтентпартнеркаллбакк:: сендмессажекомплете**, он предоставляет код результата в параметре *бстрресулт* .</span><span class="sxs-lookup"><span data-stu-id="36c46-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="36c46-126">Проигрыватель Windows Media не интерпретирует этот код результата.</span><span class="sxs-lookup"><span data-stu-id="36c46-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="36c46-127">Вместо этого проигрыватель Windows Media передает код результата вместе с обработчиком событий **онсендмессажекомплете** в параметре *result* .</span><span class="sxs-lookup"><span data-stu-id="36c46-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="36c46-128">Ни один из параметров (*MSG*, *param*, *result*) обработчика событий **Онсендмессажекомплете** не интерпретируется проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="36c46-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="36c46-129">Параметры имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="36c46-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c46-130">Требования</span><span class="sxs-lookup"><span data-stu-id="36c46-130">Requirements</span></span>



| <span data-ttu-id="36c46-131">Требование</span><span class="sxs-lookup"><span data-stu-id="36c46-131">Requirement</span></span> | <span data-ttu-id="36c46-132">Значение</span><span class="sxs-lookup"><span data-stu-id="36c46-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36c46-133">Версия</span><span class="sxs-lookup"><span data-stu-id="36c46-133">Version</span></span><br/> | <span data-ttu-id="36c46-134">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="36c46-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="36c46-135">DLL</span><span class="sxs-lookup"><span data-stu-id="36c46-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="36c46-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36c46-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c46-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36c46-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c46-138">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="36c46-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="36c46-139">**External. sendMessage**</span><span class="sxs-lookup"><span data-stu-id="36c46-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="36c46-140">**Ивмпконтентпартнер:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="36c46-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="36c46-141">**Ивмпконтентпартнеркаллбакк:: Сендмессажекомплете**</span><span class="sxs-lookup"><span data-stu-id="36c46-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





