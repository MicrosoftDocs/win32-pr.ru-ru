---
title: Иажентчарактер скрыть
description: Иажентчарактер скрыть
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069927"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="1b097-103">Иажентчарактер:: Hide</span><span class="sxs-lookup"><span data-stu-id="1b097-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="1b097-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b097-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="1b097-105">Скрывает символ.</span><span class="sxs-lookup"><span data-stu-id="1b097-105">Hides the character.</span></span>

-   <span data-ttu-id="1b097-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1b097-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="1b097-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="1b097-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="1b097-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*бфаст*</span><span class="sxs-lookup"><span data-stu-id="1b097-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="1b097-109">**Скрытие** флага анимации состояния.</span><span class="sxs-lookup"><span data-stu-id="1b097-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="1b097-110">Если этот параметр имеет **значение true**, то **Скрытая** анимация не воспроизводится до скрытия рамки символов. Если задано **значение false**, анимация будет воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="1b097-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="1b097-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="1b097-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="1b097-112">Адрес переменной, которая получает идентификатор запроса **скрытия** .</span><span class="sxs-lookup"><span data-stu-id="1b097-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="1b097-113">Сервер помещает в очередь анимацию, связанную с методом **Hide** в очереди символов.</span><span class="sxs-lookup"><span data-stu-id="1b097-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="1b097-114">Это позволяет использовать его для скрытия символа после последовательности других анимаций.</span><span class="sxs-lookup"><span data-stu-id="1b097-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="1b097-115">Вы можете воспроизвести действие немедленно с помощью метода « [**останавливаться**](iagentcharacter--stop.md) » перед вызовом метода **Hide** .</span><span class="sxs-lookup"><span data-stu-id="1b097-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="1b097-116">При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность анимации **скрытого** состояния перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="1b097-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="1b097-117">Скрытие символа может также вызвать событие [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md) другого видимого символа.</span><span class="sxs-lookup"><span data-stu-id="1b097-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="1b097-118">Скрытые символы не могут получить доступ к каналу аудио.</span><span class="sxs-lookup"><span data-stu-id="1b097-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="1b097-119">Сервер передаст состояние сбоя в событии [**рекуесткомплете**](iagentnotifysink--requestcomplete.md) , если создается запрос анимации и этот символ скрыт.</span><span class="sxs-lookup"><span data-stu-id="1b097-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b097-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="1b097-120">See Also</span></span>

[<span data-ttu-id="1b097-121">**Иажентчарактер:: показывать**</span><span class="sxs-lookup"><span data-stu-id="1b097-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 