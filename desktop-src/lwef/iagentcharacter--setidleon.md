---
title: Иажентчарактер Сетидлеон
description: Иажентчарактер Сетидлеон
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411446"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="b8f74-103">Иажентчарактер:: Сетидлеон</span><span class="sxs-lookup"><span data-stu-id="b8f74-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="b8f74-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8f74-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="b8f74-105">Задает автоматическую обработку символа в режиме простоя.</span><span class="sxs-lookup"><span data-stu-id="b8f74-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="b8f74-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b8f74-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b8f74-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Системе*</span><span class="sxs-lookup"><span data-stu-id="b8f74-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="b8f74-108">Флаг обработки бездействия.</span><span class="sxs-lookup"><span data-stu-id="b8f74-108">Idle processing flag.</span></span> <span data-ttu-id="b8f74-109">Если этот параметр имеет **значение true**, то агент Майкрософт автоматически воспроизводит анимацию состояния **состояние простоя** .</span><span class="sxs-lookup"><span data-stu-id="b8f74-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="b8f74-110">Сервер автоматически устанавливает время ожидания после последней анимации для символа.</span><span class="sxs-lookup"><span data-stu-id="b8f74-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="b8f74-111">Когда этот интервал таймера будет завершен, сервер начнет **состояние простоя** состояния для символа, воспроизводящего связанную анимацию **состояние простоя** через равные промежутки времени.</span><span class="sxs-lookup"><span data-stu-id="b8f74-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="b8f74-112">Если вы хотите управлять анимацией состояния **состояние простоя** самостоятельно, присвойте свойству значение **false**.</span><span class="sxs-lookup"><span data-stu-id="b8f74-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="b8f74-113">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="b8f74-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8f74-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="b8f74-114">See Also</span></span>

[<span data-ttu-id="b8f74-115">**Иажентчарактер:: Жетидлеон**</span><span class="sxs-lookup"><span data-stu-id="b8f74-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




