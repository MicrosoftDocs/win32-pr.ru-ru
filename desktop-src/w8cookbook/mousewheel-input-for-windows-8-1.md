---
title: Входные данные маусевхил для Windows 8.1
description: Входные данные маусевхил для Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888047"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="83eb6-103">Входные данные маусевхил для Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="83eb6-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="83eb6-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="83eb6-104">Platform</span></span>

<dl> <span data-ttu-id="83eb6-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="83eb6-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="83eb6-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="83eb6-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="83eb6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="83eb6-107">Description</span></span>

<span data-ttu-id="83eb6-108">В Windows 8.1 события маусевхил больше не доставляются на основе фокуса клавиатуры, как в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="83eb6-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="83eb6-109">В Windows 8.1 при наведении указателя мыши на приложение Магазина маусевхил будет доставлено в это приложение; Однако в целях совместимости при наведении указателя мыши на классическое приложение маусевхил будет по-прежнему доставляться на основе фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="83eb6-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="83eb6-110">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="83eb6-110">Manifestations</span></span>

<span data-ttu-id="83eb6-111">При наведении указателя мыши на приложения Магазина маусевхил прокручивает любое применимое содержимое без необходимости щелчка приложения Магазина.</span><span class="sxs-lookup"><span data-stu-id="83eb6-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="83eb6-112">Это также относится к начальному экрану.</span><span class="sxs-lookup"><span data-stu-id="83eb6-112">This also applies to the start screen.</span></span> <span data-ttu-id="83eb6-113">Это делает прокрутку, маусевхил более простое взаимодействие в Windows 8.1, чем в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83eb6-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="83eb6-114">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="83eb6-114">Mitigation</span></span>

<span data-ttu-id="83eb6-115">В большинстве случаев это изменение не должно влиять на существующие приложения.</span><span class="sxs-lookup"><span data-stu-id="83eb6-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="83eb6-116">Если приложение Магазина прослушивает события маусевхил только после того, как оно зарегистрировало событие щелчка мыши, это приложение не будет отвечать на маусевхил, пока пользователь не нащелкнул его.</span><span class="sxs-lookup"><span data-stu-id="83eb6-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="83eb6-117">Как следствие, наиболее вероятный недостаток — это просто то, что приложение продолжит работать точно так же, как и в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83eb6-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="83eb6-118">Для классических приложений наличие фокуса клавиатуры больше не дает приложению Монополи более маусевхил входных данных, но это также не приводит к разрыву этих приложений.</span><span class="sxs-lookup"><span data-stu-id="83eb6-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="83eb6-119">Поэтому краткосрочные меры защиты не требуются.</span><span class="sxs-lookup"><span data-stu-id="83eb6-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="83eb6-120">Решение</span><span class="sxs-lookup"><span data-stu-id="83eb6-120">Solution</span></span>

<span data-ttu-id="83eb6-121">Разработчики приложений Магазина должны иметь возможность получения событий маусевхил без события щелчка мыши основы.</span><span class="sxs-lookup"><span data-stu-id="83eb6-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="83eb6-122">Они не должны, например, прослушивать события маусевхил только после регистрации щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="83eb6-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="83eb6-123">Аналогичным образом, настольные приложения не должны пытаться фиксировать события маусевхил (например, установив низкоуровневые перехватчики), если они имеют фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="83eb6-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="83eb6-124">Тесты</span><span class="sxs-lookup"><span data-stu-id="83eb6-124">Tests</span></span>

<span data-ttu-id="83eb6-125">Разработчики приложений Магазина должны протестировать Windows 8.1, чтобы убедиться, что все функции прокрутки работают при наведении указателя мыши на приложение.</span><span class="sxs-lookup"><span data-stu-id="83eb6-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="83eb6-126">Разработчики классических приложений должны протестировать Windows 8.1, чтобы убедиться, что они не записывают события маусевхил (в соответствии с инструкциями выше).</span><span class="sxs-lookup"><span data-stu-id="83eb6-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




