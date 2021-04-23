---
title: Метод прерывания
description: Метод прерывания
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412968"
---
# <a name="interrupt-method"></a><span data-ttu-id="5c21d-103">Метод прерывания</span><span class="sxs-lookup"><span data-stu-id="5c21d-103">Interrupt Method</span></span>

<span data-ttu-id="5c21d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c21d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5c21d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="5c21d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5c21d-106">Прерывает анимацию для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="5c21d-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="5c21d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="5c21d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5c21d-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Запрос на прерывание* \*  </span><span class="sxs-lookup"><span data-stu-id="5c21d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="5c21d-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="5c21d-109">Part</span></span>      | <span data-ttu-id="5c21d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5c21d-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="5c21d-111">*Запрос*</span><span class="sxs-lookup"><span data-stu-id="5c21d-111">*Request*</span></span> | <span data-ttu-id="5c21d-112">Объект [**запроса**](/windows/desktop/lwef/the-request-object) для конкретного вызова анимации.</span><span class="sxs-lookup"><span data-stu-id="5c21d-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c21d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c21d-113">Remarks</span></span>

<span data-ttu-id="5c21d-114">Его можно использовать для синхронизации анимации между символами.</span><span class="sxs-lookup"><span data-stu-id="5c21d-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="5c21d-115">Например, если другой символ находится в циклической анимации, этот метод останавливает цикл и переходит к следующей анимации в очереди символов.</span><span class="sxs-lookup"><span data-stu-id="5c21d-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="5c21d-116">Нельзя прерывать неиспользуемую анимацию символов (которая не была загружена).</span><span class="sxs-lookup"><span data-stu-id="5c21d-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="5c21d-117">Чтобы указать параметр запроса, необходимо создать переменную и назначить запрос анимации, который нужно прервать:</span><span class="sxs-lookup"><span data-stu-id="5c21d-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="5c21d-118">Нельзя прерывать анимацию того же символа, который указан в этом методе, так как сервер помещает метод **прерывания** в очередь анимации этого символа.</span><span class="sxs-lookup"><span data-stu-id="5c21d-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="5c21d-119">Таким образом, **прерывание** можно использовать только для остановки анимации другого символа, который вы загрузили.</span><span class="sxs-lookup"><span data-stu-id="5c21d-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="5c21d-120">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="5c21d-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="5c21d-121">**Прерывание** не приводит к сбросу очереди символов. Она останавливает существующую анимацию и переходит к следующей анимации в очереди символов.</span><span class="sxs-lookup"><span data-stu-id="5c21d-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="5c21d-122">Чтобы остановить и очистить очередь символов, используйте метод [**остановки**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="5c21d-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5c21d-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="5c21d-123">See Also</span></span>

[<span data-ttu-id="5c21d-124">**Метод Stop**</span><span class="sxs-lookup"><span data-stu-id="5c21d-124">**Stop method**</span></span>](stop-method.md)


 

 