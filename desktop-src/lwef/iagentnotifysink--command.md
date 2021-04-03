---
title: Команда Иажентнотифисинк
description: Команда Иажентнотифисинк
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987446"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="465c7-103">Иажентнотифисинк:: Command</span><span class="sxs-lookup"><span data-stu-id="465c7-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="465c7-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="465c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="465c7-105">Уведомляет клиентское приложение о том, что [**команда**](/windows/desktop/lwef/the-command-object) была выбрана пользователем.</span><span class="sxs-lookup"><span data-stu-id="465c7-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="465c7-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="465c7-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="465c7-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*двкоммандид*</span><span class="sxs-lookup"><span data-stu-id="465c7-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="465c7-108">Идентификатор альтернативы для команды наилучшего соответствия.</span><span class="sxs-lookup"><span data-stu-id="465c7-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="465c7-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*пункусеринпут*</span><span class="sxs-lookup"><span data-stu-id="465c7-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="465c7-110">Адрес интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для объекта [**иажентусеринпут**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="465c7-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="465c7-111">Используйте [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения интерфейса [**иажентусеринпут**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="465c7-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="465c7-112">Сервер оповещает входной-активный клиент, когда пользователь выбирает команду с помощью голоса или выбирая команду во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="465c7-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="465c7-113">Это событие возникает, даже если пользователь выбирает одну из команд сервера.</span><span class="sxs-lookup"><span data-stu-id="465c7-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="465c7-114">В этом случае сервер возвращает идентификатор команды null, оценку достоверности и голосовой текст, возвращенный модулем распознавания речи для этой записи.</span><span class="sxs-lookup"><span data-stu-id="465c7-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="465c7-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="465c7-115">See Also</span></span>

[<span data-ttu-id="465c7-116">**иажентусеринпут**</span><span class="sxs-lookup"><span data-stu-id="465c7-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 