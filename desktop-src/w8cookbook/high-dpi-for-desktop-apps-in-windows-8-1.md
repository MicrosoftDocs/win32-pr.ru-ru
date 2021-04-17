---
title: Высокое разрешение для настольных приложений в Windows 8.1
description: Высокое разрешение для настольных приложений в Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700887"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="c81ec-103">Высокое разрешение для настольных приложений в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c81ec-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="c81ec-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="c81ec-104">Platforms</span></span>

<dl> <span data-ttu-id="c81ec-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c81ec-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="c81ec-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c81ec-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="c81ec-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c81ec-107">Description</span></span>

<span data-ttu-id="c81ec-108">В Windows 8.1 Классические приложения должны выполняться на экранах с масштабированием 200% в дополнение к масштабированию 100%, 125% и 150%, которое поддерживается в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c81ec-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="c81ec-109">Кроме того, настольные приложения масштабируются на уровне отдельных мониторов, а не в один коэффициент масштабирования, применяемый ко всем экранам.</span><span class="sxs-lookup"><span data-stu-id="c81ec-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="c81ec-110">Разработчики также могут вызывать новые API в Windows 8.1 для получения коэффициентов масштабирования для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="c81ec-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="c81ec-111">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="c81ec-111">Manifestations</span></span>

<span data-ttu-id="c81ec-112">Пользователи могут использовать новые высокоплотные экраны с Windows 8.1 для наглядного визуального интерфейса, который использует преимущества более высоких пиксельных данных.</span><span class="sxs-lookup"><span data-stu-id="c81ec-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="c81ec-113">Если приложения не обрабатывали высокое разрешение DPI, Windows будет масштабировать их для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c81ec-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="c81ec-114">Кроме того, пользователи могут использовать сочетание высокой и низкой плотности на одном компьютере, и Windows будет масштабировать содержимое соответствующим образом для каждого дисплея.</span><span class="sxs-lookup"><span data-stu-id="c81ec-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="c81ec-115">Это улучшение по сравнению с Windows 8, где содержимое может быть слишком большим для некоторых экранов.</span><span class="sxs-lookup"><span data-stu-id="c81ec-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c81ec-116">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="c81ec-116">Mitigation</span></span>

<span data-ttu-id="c81ec-117">Поскольку Windows масштабирует приложения, которые не масштабируются самостоятельно, разработчики, как правило, не должны выполнять дополнительную работу, но разработчики, которые вкладываются в написание приложений, поддерживающих высокое разрешение, будут иметь конкурентное преимущество, так как эти приложения будут лучше выглядят на новых ноутбуках с высоким разрешением и мониторов настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c81ec-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="c81ec-118">Решение</span><span class="sxs-lookup"><span data-stu-id="c81ec-118">Solution</span></span>

<span data-ttu-id="c81ec-119">Создание приложения, которое может воспользоваться преимуществами высокого DPI, — сложная задача по проектированию и реализации.</span><span class="sxs-lookup"><span data-stu-id="c81ec-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="c81ec-120">Ниже приведены ссылки на сведения о учебниках, создании содержимого презентаций и подобной поддержке.</span><span class="sxs-lookup"><span data-stu-id="c81ec-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="c81ec-121">Тесты</span><span class="sxs-lookup"><span data-stu-id="c81ec-121">Tests</span></span>

<span data-ttu-id="c81ec-122">Даже если разработчики не решили заставить приложения использовать преимущества высокого DPI, они должны протестировать свое приложение на 100%, 125%, 150% и 200% масштабирования, чтобы обеспечить удовлетворительное и конкурентное взаимодействие с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="c81ec-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="c81ec-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="c81ec-123">Resources</span></span>

-   [<span data-ttu-id="c81ec-124">Технический документ и руководство по высокому DPI в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c81ec-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="c81ec-125">Примеры программ для Windows Desktop</span><span class="sxs-lookup"><span data-stu-id="c81ec-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="c81ec-126">Сборка сеанса 2013 с высоким разрешением в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c81ec-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 