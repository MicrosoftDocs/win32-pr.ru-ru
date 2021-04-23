---
description: Определение допустимых операций DVD
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Определение допустимых операций DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423037"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="e5d55-103">Определение допустимых операций DVD</span><span class="sxs-lookup"><span data-stu-id="e5d55-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="e5d55-104">Существует несколько факторов, которые определяют, можно ли выполнять заданную операцию DVD:</span><span class="sxs-lookup"><span data-stu-id="e5d55-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="e5d55-105">Текущий домен.</span><span class="sxs-lookup"><span data-stu-id="e5d55-105">The current domain.</span></span> <span data-ttu-id="e5d55-106">Некоторые команды допустимы только в определенных доменах.</span><span class="sxs-lookup"><span data-stu-id="e5d55-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="e5d55-107">При изменении домена навигатор отправляет \_ \_ событие изменения домена на DVD-диске EC \_ .</span><span class="sxs-lookup"><span data-stu-id="e5d55-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="e5d55-108">Чтобы получить текущий домен, можно также вызвать [**IDvdInfo2:: жеткуррентдомаин**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) .</span><span class="sxs-lookup"><span data-stu-id="e5d55-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="e5d55-109">Флаги УОПС.</span><span class="sxs-lookup"><span data-stu-id="e5d55-109">UOPS flags.</span></span> <span data-ttu-id="e5d55-110">Это флаги, записанные на диск, указывающие, какие операции разрешены.</span><span class="sxs-lookup"><span data-stu-id="e5d55-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="e5d55-111">Всякий раз при изменении флагов навигатор отправляет \_ событие УОПС Change, допустимое в формате EC DVD, \_ \_ \_ с новыми флагами.</span><span class="sxs-lookup"><span data-stu-id="e5d55-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="e5d55-112">Можно также вызвать метод [**IDvdInfo2:: жеткуррентуопс**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) , чтобы получить текущие флаги УОПС.</span><span class="sxs-lookup"><span data-stu-id="e5d55-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="e5d55-113">Содержимое DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="e5d55-113">DVD content.</span></span> <span data-ttu-id="e5d55-114">Некоторые команды могут быть неактуальными в зависимости от содержимого DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="e5d55-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="e5d55-115">Например, метод [**IDvdControl2:: селектангле**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) может быть разрешен в соответствии с флагами текущего домена и УОПС, но у видео может быть только один угол.</span><span class="sxs-lookup"><span data-stu-id="e5d55-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="e5d55-116">В этом случае вызов **селектангле** разрешается, но не является значимым параметром.</span><span class="sxs-lookup"><span data-stu-id="e5d55-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="e5d55-117">Если вы сомневаетесь, разрешите действие.</span><span class="sxs-lookup"><span data-stu-id="e5d55-117">When in doubt, permit an action.</span></span> <span data-ttu-id="e5d55-118">В худшем случае метод [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) завершится ошибкой, и вы сможете отправить отзыв пользователю.</span><span class="sxs-lookup"><span data-stu-id="e5d55-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="e5d55-119">Обратная связь должна быть относительно ненавязчивой.</span><span class="sxs-lookup"><span data-stu-id="e5d55-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="e5d55-120">Например, вы можете мгновенно предупредить пользователя к маленькому красному крестику.</span><span class="sxs-lookup"><span data-stu-id="e5d55-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="e5d55-121">Навигатор DVD возвращает \_ \_ DVD-диск VFW e \_ INVALIDDOMAIN, когда домен запрещает операцию, и \_ \_ Операция ДИСКового DVD-диска VFW была \_ \_ запрещена, когда флаги УОПС запрещают операцию.</span><span class="sxs-lookup"><span data-stu-id="e5d55-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d55-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e5d55-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d55-123">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="e5d55-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



