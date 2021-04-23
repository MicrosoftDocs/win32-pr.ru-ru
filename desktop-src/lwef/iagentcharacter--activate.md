---
title: Активация Иажентчарактер
description: Активация Иажентчарактер
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532507"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="15c4a-103">Иажентчарактер:: Activate</span><span class="sxs-lookup"><span data-stu-id="15c4a-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="15c4a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15c4a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="15c4a-105">Указывает, является ли клиент активным, или символ является самым верхним.</span><span class="sxs-lookup"><span data-stu-id="15c4a-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="15c4a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15c4a-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="15c4a-107">Возвращает \_ значение false, указывающее, что операция не была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15c4a-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="15c4a-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*сстате*</span><span class="sxs-lookup"><span data-stu-id="15c4a-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="15c4a-109">Для этого параметра можно указать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="15c4a-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="15c4a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="15c4a-110">Value</span></span> | <span data-ttu-id="15c4a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="15c4a-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="15c4a-112">0</span><span class="sxs-lookup"><span data-stu-id="15c4a-112">0</span></span>     | <span data-ttu-id="15c4a-113">Задать как не активный клиент.</span><span class="sxs-lookup"><span data-stu-id="15c4a-113">Set as not the active client.</span></span> |
| <span data-ttu-id="15c4a-114">1</span><span class="sxs-lookup"><span data-stu-id="15c4a-114">1</span></span>     | <span data-ttu-id="15c4a-115">Установите в качестве активного клиента.</span><span class="sxs-lookup"><span data-stu-id="15c4a-115">Set as the active client.</span></span>     |
| <span data-ttu-id="15c4a-116">2</span><span class="sxs-lookup"><span data-stu-id="15c4a-116">2</span></span>     | <span data-ttu-id="15c4a-117">Сделайте самый верхний символ.</span><span class="sxs-lookup"><span data-stu-id="15c4a-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="15c4a-118">Если отображается несколько символов, только один из них получит речевой ввод за раз.</span><span class="sxs-lookup"><span data-stu-id="15c4a-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="15c4a-119">Аналогично, если несколько клиентских приложений совместно используют один и тот же символ, только одна из них получает ввод с клавиатуры (например, элемент управления агента Microsoft Agent по щелчку или перетаскиванию событий) за раз.</span><span class="sxs-lookup"><span data-stu-id="15c4a-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="15c4a-120">Кодировка для получения входных данных мыши и речи — самый верхний символ, а клиент, принимающий входные данные, — это активный клиент символа.</span><span class="sxs-lookup"><span data-stu-id="15c4a-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="15c4a-121">(Окно с самым верхним символом также отображается в верхней части z-порядка окна символов.) Как правило, пользователь определяет, какой символ является самым верхним, путем явного выбора.</span><span class="sxs-lookup"><span data-stu-id="15c4a-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="15c4a-122">Однако самая верхняя активация также изменяется при отображении или скрытии символа (он становится или больше не выше самого верхнего, соответственно).</span><span class="sxs-lookup"><span data-stu-id="15c4a-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="15c4a-123">Этот метод также можно использовать для явного управления тем, когда клиент получает входные данные, направленные на символ, например, когда само приложение станет активным.</span><span class="sxs-lookup"><span data-stu-id="15c4a-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="15c4a-124">Например, если задать для параметра **State** значение 2, то символ будет самым верхним, а клиент получит все события мыши и речевого ввода, созданные при взаимодействии пользователя с этим символом.</span><span class="sxs-lookup"><span data-stu-id="15c4a-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="15c4a-125">Таким образом, он также делает клиент клиентом для ввода активного символа.</span><span class="sxs-lookup"><span data-stu-id="15c4a-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="15c4a-126">Однако можно также задать для активного клиента символ, не выполняя самого верхнего символа, установив для параметра **State** значение 1.</span><span class="sxs-lookup"><span data-stu-id="15c4a-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="15c4a-127">Это позволяет клиенту получить входные данные, направленные на этот символ, когда символ станет самым верхним.</span><span class="sxs-lookup"><span data-stu-id="15c4a-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="15c4a-128">Аналогичным образом можно настроить клиент так, чтобы он не был активным клиентом (чтобы не получать входные данные), когда символ станет самым верхним, установив для параметра **State** значение 0.</span><span class="sxs-lookup"><span data-stu-id="15c4a-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="15c4a-129">Вы можете определить, есть ли у символа другие текущие клиенты, использующие [**иажентчарактер:: хасосерклиентс**](iagentcharacter--hasotherclients.md).</span><span class="sxs-lookup"><span data-stu-id="15c4a-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="15c4a-130">Избегайте вызова этого метода непосредственно после метода [**представления**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="15c4a-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="15c4a-131">**Показывать** автоматически задает клиент input-Active.</span><span class="sxs-lookup"><span data-stu-id="15c4a-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="15c4a-132">Если символ скрыт, вызов функции **Activate** может завершиться ошибкой, если он будет обработан до завершения метода **представления** .</span><span class="sxs-lookup"><span data-stu-id="15c4a-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="15c4a-133">Попытка вызвать этот метод с параметром **State** , равным 2 (если указанный символ скрыт), приведет к сбою.</span><span class="sxs-lookup"><span data-stu-id="15c4a-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="15c4a-134">Аналогично, если задать для параметра **State** значение 0, а приложение является единственным клиентом, этот вызов завершается неудачно.</span><span class="sxs-lookup"><span data-stu-id="15c4a-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="15c4a-135">Символ всегда должен иметь самый верхний клиент.</span><span class="sxs-lookup"><span data-stu-id="15c4a-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="15c4a-136">Вызов этого метода с **состоянием** , установленным в значение 1, обычно не создает событие [**Ажентнотифисинк:: активатеинпутстате**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) , если другие символы не загружены или приложение уже не содержит активных входных данных.</span><span class="sxs-lookup"><span data-stu-id="15c4a-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="15c4a-137">См. также:</span><span class="sxs-lookup"><span data-stu-id="15c4a-137">See Also</span></span>

[<span data-ttu-id="15c4a-138">**Иажентчарактер:: Хасосерклиентс**</span><span class="sxs-lookup"><span data-stu-id="15c4a-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




