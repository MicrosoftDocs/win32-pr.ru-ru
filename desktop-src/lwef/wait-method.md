---
title: Метод Wait
description: Метод Wait
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710257"
---
# <a name="wait-method"></a><span data-ttu-id="1919e-103">Метод Wait</span><span class="sxs-lookup"><span data-stu-id="1919e-103">Wait Method</span></span>

<span data-ttu-id="1919e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1919e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1919e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="1919e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1919e-106">Заставляет очередь анимации для указанного символа ожидать завершения заданного запроса анимации.</span><span class="sxs-lookup"><span data-stu-id="1919e-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="1919e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1919e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1919e-108">\*Агент ***. Символы ("*** чарактерид \*\*\*"). Запрос на ожидание\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1919e-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="1919e-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="1919e-109">Part</span></span>      | <span data-ttu-id="1919e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1919e-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="1919e-111">*Запрос*</span><span class="sxs-lookup"><span data-stu-id="1919e-111">*Request*</span></span> | <span data-ttu-id="1919e-112">Объект [**запроса**](/windows/desktop/lwef/the-request-object) , указывающий определенную анимацию..</span><span class="sxs-lookup"><span data-stu-id="1919e-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1919e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1919e-113">Remarks</span></span>

<span data-ttu-id="1919e-114">Этот метод следует использовать только в том случае, если поддерживается несколько (одновременных) символов и выполняется попытка последовательного взаимодействия символов.</span><span class="sxs-lookup"><span data-stu-id="1919e-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="1919e-115">(Для одного символа каждый запрос анимации воспроизводится последовательно — по завершении предыдущего запроса.) Если у вас есть два символа и требуется, чтобы запрос анимации символа ожидал завершения анимации другого символа, задайте метод **ожидания** для объекта [**запроса**](/windows/desktop/lwef/the-request-object) анимации другого символа.</span><span class="sxs-lookup"><span data-stu-id="1919e-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="1919e-116">Чтобы указать параметр запроса, необходимо создать переменную и назначить запрос анимации, который нужно прервать:</span><span class="sxs-lookup"><span data-stu-id="1919e-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



<span data-ttu-id="1919e-117">Можно также упростить код, просто вызвав **Wait** напрямую, используя конкретный запрос анимации.</span><span class="sxs-lookup"><span data-stu-id="1919e-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="1919e-118">Это позволяет избежать явного объявления объекта [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="1919e-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 