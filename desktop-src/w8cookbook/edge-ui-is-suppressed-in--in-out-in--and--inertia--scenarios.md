---
title: ИНТЕРФЕЙС пограничной панели подавляется в сценариях "встроенные" и "инерция"
description: ИНТЕРФЕЙС пограничной панели подавляется в сценариях "встроенные" и "инерция"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258971"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="980d0-103">ИНТЕРФЕЙС пограничной панели подавляется в сценариях "встроенные" и "инерция"</span><span class="sxs-lookup"><span data-stu-id="980d0-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="980d0-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="980d0-104">Platform</span></span>

<dl> <span data-ttu-id="980d0-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="980d0-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="980d0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="980d0-106">Description</span></span>

<span data-ttu-id="980d0-107">В некоторых случаях пользователи могут случайно вызывать интерфейс пользователя с ребром (чудо, панель приложений, переключение приложений).</span><span class="sxs-lookup"><span data-stu-id="980d0-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="980d0-108">Мы предоставили функцию, позволяющую разработчикам проектировать свой пользовательский интерфейс для всего экрана, не делая аффорданцес (например, границы), чтобы предотвратить случайное попадание на края.</span><span class="sxs-lookup"><span data-stu-id="980d0-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="980d0-109">Существует два варианта, которые могут привести к непреднамеренному появлению случайных пограничных прокруток:</span><span class="sxs-lookup"><span data-stu-id="980d0-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="980d0-110">В быстром панорамировании скорость и точность взаимодействия иногда могут привести к тому, что они поступают от края экрана.</span><span class="sxs-lookup"><span data-stu-id="980d0-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="980d0-111">Если пользователи быстро оставляют и повторно вводят область экрана при рукописном вводе с помощью пальца, например в приложении для рисования, это последующее поведение может по ошибке запустить интерфейс пользователя и прервать работу пользователя.</span><span class="sxs-lookup"><span data-stu-id="980d0-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="980d0-112">Чтобы повысить удобство работы пользователя и разработчика, Пользовательский интерфейс пограничной панели будет подавлен в двух конкретных экземплярах:</span><span class="sxs-lookup"><span data-stu-id="980d0-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="980d0-113">Когда пользователь выполняет панорамирование в приложении, поддерживающем Дманип инерцию, и просчитывается за пределами экрана во время инерции, Пользовательский интерфейс ребра не будет вызываться в окне времени ожидания</span><span class="sxs-lookup"><span data-stu-id="980d0-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="980d0-114">При использовании сертифицированных устройств, когда пользователь быстро насчитывается с экрана и выходит из него (во время перемещения) в пределах определенных параметров, Пользовательский интерфейс не будет вызываться.</span><span class="sxs-lookup"><span data-stu-id="980d0-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="980d0-115">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="980d0-115">Manifestations</span></span>

<span data-ttu-id="980d0-116">Пользователи быстро проводят прокрутку на сторону, а использование приложения приведет к снижению непреднамеренного вызова ребра.</span><span class="sxs-lookup"><span data-stu-id="980d0-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="980d0-117">Решение</span><span class="sxs-lookup"><span data-stu-id="980d0-117">Solution</span></span>

<span data-ttu-id="980d0-118">Разработчикам следует помнить об этих угрозах и иметь возможность использовать весь экран, не опасаясь, что пользователи случайно активируют пользовательский интерфейс при взаимодействии с приложением на границе.</span><span class="sxs-lookup"><span data-stu-id="980d0-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




