---
title: Метод завершения (устаревшие функции среды Windows)
description: Метод Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701013"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="319f9-103">Метод завершения (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="319f9-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="319f9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="319f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="319f9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="319f9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="319f9-106">Останавливает анимацию для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="319f9-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="319f9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="319f9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="319f9-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[ *Запрос* на завершение\]</span><span class="sxs-lookup"><span data-stu-id="319f9-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="319f9-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="319f9-109">Part</span></span>      | <span data-ttu-id="319f9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="319f9-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="319f9-111">*Запрос*</span><span class="sxs-lookup"><span data-stu-id="319f9-111">*Request*</span></span> | <span data-ttu-id="319f9-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="319f9-112">Optional.</span></span> <span data-ttu-id="319f9-113">Объект [**запроса**](/windows/desktop/lwef/the-request-object) , указывающий конкретный вызов анимации.</span><span class="sxs-lookup"><span data-stu-id="319f9-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="319f9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="319f9-114">Remarks</span></span>

<span data-ttu-id="319f9-115">Чтобы указать параметр запроса, необходимо создать переменную и назначить запрос анимации, который нужно присвоить.</span><span class="sxs-lookup"><span data-stu-id="319f9-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="319f9-116">Если параметр **запроса** не задан, сервер останавливает все анимации для символа, включая вызовы [**Get**](get-method.md) , помещенные в очередь, и очищает ее очередь анимации, если этот символ в данный момент не содержит **скрытую** анимацию или не **отображает** ее.</span><span class="sxs-lookup"><span data-stu-id="319f9-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="319f9-117">Этот метод не останавливает вызовы **Get** , не входящие в очередь.</span><span class="sxs-lookup"><span data-stu-id="319f9-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="319f9-118">Чтобы отменить определенную анимацию или вызов [**Get**](get-method.md) , объявите объектную переменную и назначьте запрос анимации этой переменной:</span><span class="sxs-lookup"><span data-stu-id="319f9-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="319f9-119">Этот метод не создаст объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="319f9-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="319f9-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="319f9-120">See Also</span></span>

[<span data-ttu-id="319f9-121">**Метод Стопалл**</span><span class="sxs-lookup"><span data-stu-id="319f9-121">**StopAll method**</span></span>](stopall-method.md)


 

 
