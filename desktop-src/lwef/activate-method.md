---
title: Метод Activate
description: Метод Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691486"
---
# <a name="activate-method"></a><span data-ttu-id="6df92-103">Метод Activate</span><span class="sxs-lookup"><span data-stu-id="6df92-103">Activate Method</span></span>

<span data-ttu-id="6df92-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6df92-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6df92-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Nописание**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="6df92-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="6df92-106">Задает активный клиент или символ.</span><span class="sxs-lookup"><span data-stu-id="6df92-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="6df92-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6df92-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6df92-108">\*Агент ***. Символы ("*** чарактерид \* \* *").* \*  \[ *Состояние* активации\]</span><span class="sxs-lookup"><span data-stu-id="6df92-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="6df92-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="6df92-109">Part</span></span>    | <span data-ttu-id="6df92-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6df92-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df92-111">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="6df92-111">*State*</span></span> | <span data-ttu-id="6df92-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6df92-112">Optional.</span></span> <span data-ttu-id="6df92-113">Для этого параметра можно указать следующие значения: 0 — не активный клиент.</span><span class="sxs-lookup"><span data-stu-id="6df92-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="6df92-114">1 активный клиент.</span><span class="sxs-lookup"><span data-stu-id="6df92-114">1 The active client.</span></span> <br/> <span data-ttu-id="6df92-115">2 (по умолчанию) верхний символ.</span><span class="sxs-lookup"><span data-stu-id="6df92-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6df92-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6df92-116">Remarks</span></span>

<span data-ttu-id="6df92-117">Если отображается несколько символов, только один из них получит речевой ввод за раз.</span><span class="sxs-lookup"><span data-stu-id="6df92-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="6df92-118">Аналогично, если несколько клиентских приложений совместно используют один и тот же символ, только одна из них получает ввод мыши (например, элемент управления агента Microsoft Agent щелкнул или перетаскивает события).</span><span class="sxs-lookup"><span data-stu-id="6df92-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="6df92-119">Кодировка для получения входных данных мыши и речи — самый верхний символ, а клиент, получающий входные данные, — это активный клиент этого символа.</span><span class="sxs-lookup"><span data-stu-id="6df92-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="6df92-120">(Окно с самым верхним символом также отображается в верхней части z-порядка окна символов.) Как правило, пользователь определяет верхний символ путем явного выбора символа.</span><span class="sxs-lookup"><span data-stu-id="6df92-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="6df92-121">Однако самая верхняя активация также изменяется при отображении или скрытии символа (он становится или больше не выше самого верхнего, соответственно).</span><span class="sxs-lookup"><span data-stu-id="6df92-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="6df92-122">Этот метод также можно использовать для явного управления тем, когда клиент получает входные данные, направленные на символ, например, когда само приложение станет активным.</span><span class="sxs-lookup"><span data-stu-id="6df92-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="6df92-123">Например, если задать для параметра *State* значение 2, то символ верхнего уровня и клиент получит все события ввода речи и речевых сообщений, созданные при взаимодействии пользователя с этим символом.</span><span class="sxs-lookup"><span data-stu-id="6df92-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="6df92-124">Таким образом, он также делает клиент клиентом для ввода активного символа.</span><span class="sxs-lookup"><span data-stu-id="6df92-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="6df92-125">Однако вы также можете задать для себя активный клиент для символа, не выполняя его самым верхним, установив для параметра *State* значение 1.</span><span class="sxs-lookup"><span data-stu-id="6df92-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="6df92-126">Это позволяет клиенту получить входные данные, направленные на этот символ, когда символ станет самым верхним.</span><span class="sxs-lookup"><span data-stu-id="6df92-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="6df92-127">Аналогичным образом можно настроить клиент так, чтобы он не был активным клиентом (не получать входные данные), когда символ станет самым верхним, установив для параметра *State* значение 0.</span><span class="sxs-lookup"><span data-stu-id="6df92-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="6df92-128">Избегайте вызова этого метода непосредственно после метода [**представления**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) .</span><span class="sxs-lookup"><span data-stu-id="6df92-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="6df92-129">**Показывать** автоматически задает клиент input-Active.</span><span class="sxs-lookup"><span data-stu-id="6df92-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="6df92-130">Если символ скрыт, вызов [**активации**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) может завершиться ошибкой, если он будет обработан до завершения метода **представления** .</span><span class="sxs-lookup"><span data-stu-id="6df92-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="6df92-131">При вызове этого метода для функции он возвращает логическое значение, указывающее, был ли метод обработан удачно.</span><span class="sxs-lookup"><span data-stu-id="6df92-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="6df92-132">Попытка вызвать этот метод с параметром *State* , равным 2, если указанный символ является скрытым, приведет к сбою.</span><span class="sxs-lookup"><span data-stu-id="6df92-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="6df92-133">Аналогично, если задать для параметра *State* значение 0, а приложение является единственным клиентом, этот вызов завершается неудачей, поскольку символ должен всегда иметь самый верхний клиент.</span><span class="sxs-lookup"><span data-stu-id="6df92-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="6df92-134">Вызов этого метода с *состоянием* , установленным в значение 1, обычно не создает событие [**активатеинпут**](https://www.bing.com/search?q=**ActivateInput**) , если другие символы не загружены или приложение уже находится в режиме ввода.</span><span class="sxs-lookup"><span data-stu-id="6df92-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6df92-135">См. также:</span><span class="sxs-lookup"><span data-stu-id="6df92-135">See Also</span></span>

<span data-ttu-id="6df92-136">[**Событие активатеинпут**](activateinput-event.md), [ **событие деактиватеинпут**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="6df92-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

