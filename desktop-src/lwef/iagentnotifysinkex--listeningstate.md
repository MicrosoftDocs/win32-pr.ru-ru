---
title: Иажентнотифисинкекс Листенингстате
description: Иажентнотифисинкекс Листенингстате
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532213"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="f42ac-103">Иажентнотифисинкекс:: Листенингстате</span><span class="sxs-lookup"><span data-stu-id="f42ac-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="f42ac-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f42ac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="f42ac-105">Уведомляет клиентское приложение при изменении режима прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f42ac-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="f42ac-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f42ac-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="f42ac-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*двчарактерид*</span><span class="sxs-lookup"><span data-stu-id="f42ac-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="f42ac-108">Символ, для которого изменилось состояние прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f42ac-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="f42ac-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*блистенинг*</span><span class="sxs-lookup"><span data-stu-id="f42ac-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="f42ac-110">Состояние режима прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f42ac-110">The Listening mode state.</span></span> <span data-ttu-id="f42ac-111">**Значение true** указывает, что режим прослушивания запущен; **Значение false**, если режим прослушивания завершен.</span><span class="sxs-lookup"><span data-stu-id="f42ac-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="f42ac-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*двкаусе*</span><span class="sxs-lookup"><span data-stu-id="f42ac-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="f42ac-113">Причиной события может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f42ac-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="f42ac-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f42ac-114">Value</span></span>                                                                             | <span data-ttu-id="f42ac-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f42ac-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f42ac-116">**const беззнаковое длинное** **лскомплете \_ Причина \_ програмдисаблед = 1;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="f42ac-117">Режим прослушивания был отключен программным кодом.</span><span class="sxs-lookup"><span data-stu-id="f42ac-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="f42ac-118">**const беззнаковое длинное** **лскомплете \_ Причина \_ програмтимедаут = 2;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="f42ac-119">Истекло время ожидания режима прослушивания (включенного программным кодом).</span><span class="sxs-lookup"><span data-stu-id="f42ac-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="f42ac-120">**const беззнаковое длинное** **лскомплете \_ Причина \_ усертимедаут = 3;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="f42ac-121">Истекло время ожидания режима прослушивания (включенного с помощью ключа прослушивания).</span><span class="sxs-lookup"><span data-stu-id="f42ac-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="f42ac-122">**const беззнаковое длинное** **лскомплете \_ Причина \_ усеррелеаседкэй = 4;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="f42ac-123">Режим прослушивания отключен, так как пользователь освободил ключ прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f42ac-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="f42ac-124">**const беззнаковое длинное** **лскомплете \_ Причина \_ усеруттеранцеендед = 5;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="f42ac-125">Режим прослушивания отключен, так как пользователь завершил диктовку.</span><span class="sxs-lookup"><span data-stu-id="f42ac-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="f42ac-126">**const беззнаковое длинное** **лскомплете \_ Причина \_ клиентдеактиватед = 6;**</span><span class="sxs-lookup"><span data-stu-id="f42ac-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="f42ac-127">Режим прослушивания отключен, так как входной активный клиент был деактивирован.</span><span class="sxs-lookup"><span data-stu-id="f42ac-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="f42ac-128">**const беззнаковое длинное** **лскомплете \_ Причина \_ дефаултчарчанже = 7**</span><span class="sxs-lookup"><span data-stu-id="f42ac-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="f42ac-129">Режим прослушивания отключен, так как был изменен символ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f42ac-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="f42ac-130">**const беззнаковое длинное** **лскомплете \_ Причина \_ усердисаблед = 8**</span><span class="sxs-lookup"><span data-stu-id="f42ac-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="f42ac-131">Режим прослушивания отключен, так как пользователь отключил речевой ввод.</span><span class="sxs-lookup"><span data-stu-id="f42ac-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="f42ac-132">Это событие отправляется всем клиентам, когда режим прослушивания начинается после того, как пользователь нажимает клавишу прослушивания или когда истекает время ожидания, или когда входящий-активный клиент вызывает метод [**иажентчарактерекс:: Listen**](iagentcharacterex--listen.md) со значением **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="f42ac-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="f42ac-133">Событие возвращает значения для клиентов, которые в настоящий момент загрузили этот символ.</span><span class="sxs-lookup"><span data-stu-id="f42ac-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="f42ac-134">Все остальные клиенты получают символ null (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="f42ac-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="f42ac-135">См. также:</span><span class="sxs-lookup"><span data-stu-id="f42ac-135">See Also</span></span>

[<span data-ttu-id="f42ac-136">**Иажентчарактерекс:: Listen**</span><span class="sxs-lookup"><span data-stu-id="f42ac-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





