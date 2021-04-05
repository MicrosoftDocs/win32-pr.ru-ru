---
title: Иажентчарактер Play
description: Иажентчарактер Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068662"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="4328f-103">Иажентчарактер::Pный макет</span><span class="sxs-lookup"><span data-stu-id="4328f-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="4328f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4328f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="4328f-105">Воспроизводит указанную анимацию.</span><span class="sxs-lookup"><span data-stu-id="4328f-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="4328f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4328f-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="4328f-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="4328f-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="4328f-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*бсзаниматион*</span><span class="sxs-lookup"><span data-stu-id="4328f-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="4328f-109">Имя анимации.</span><span class="sxs-lookup"><span data-stu-id="4328f-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="4328f-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="4328f-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="4328f-111">Адрес переменной, которая получает идентификатор запроса **иажентчарактер::P** .</span><span class="sxs-lookup"><span data-stu-id="4328f-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="4328f-112">Имя анимации определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4328f-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4328f-113">Прежде чем воспроизводить указанную анимацию, сервер пытается воспроизвести анимацию **возврата** для предыдущей анимации (если она была назначена).</span><span class="sxs-lookup"><span data-stu-id="4328f-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="4328f-114">Если данные анимации персонажа хранятся на локальном компьютере пользователя, можно использовать метод **иажентчарактер::P макетирования** и указать имя анимации.</span><span class="sxs-lookup"><span data-stu-id="4328f-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="4328f-115">При использовании протокола HTTP для доступа к данным анимации используйте метод [**Prepare**](iagentcharacter--prepare.md) , чтобы обеспечить доступность анимации перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="4328f-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="4328f-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="4328f-116">See Also</span></span>

[<span data-ttu-id="4328f-117">**Иажентчарактер::P готовка**</span><span class="sxs-lookup"><span data-stu-id="4328f-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




