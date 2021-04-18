---
title: Active Accessibility и автоматизация пользовательского интерфейса
description: Microsoft Active Accessibility предназначен для использования с операционными системами Windows XP и более ранних версий.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700693"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="31d94-103">Active Accessibility и автоматизация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="31d94-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="31d94-104">Microsoft Active Accessibility предназначен для использования с операционными системами Windows XP и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="31d94-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="31d94-105">Разработчикам пользовательских элементов управления и доступных технологических клиентских приложений для Windows XP и Windows Vista рекомендуется использовать технологию Microsoft [UI Automation](entry-uiauto-win32.md) .</span><span class="sxs-lookup"><span data-stu-id="31d94-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="31d94-106">Автоматизация пользовательского интерфейса Майкрософт — это полнофункциональная система, которая предоставляет более точную информацию о пользовательском интерфейсе и предоставляет пользователю больше возможностей для взаимодействия с элементами управления.</span><span class="sxs-lookup"><span data-stu-id="31d94-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="31d94-107">В частности, он обеспечивает значительно расширенную поддержку текста.</span><span class="sxs-lookup"><span data-stu-id="31d94-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="31d94-108">Набор прокси-объектов обеспечивает поддержку автоматизации пользовательского интерфейса для стандартных элементов управления Microsoft Win32 и Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="31d94-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="31d94-109">Расширенная поддержка доступна для элементов управления, специально написанных с помощью модели автоматизации пользовательского интерфейса, включая элементы машинного Windows Presentation Foundation (WPF), которые не поддерживают непосредственно Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="31d94-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="31d94-110">Пользовательские элементы управления, поддерживающие автоматизацию пользовательского интерфейса, могут быть написаны как в управляемом, так и в неуправляемом коде.</span><span class="sxs-lookup"><span data-stu-id="31d94-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="31d94-111">Клиенты Microsoft Active Accessibility имеют ограниченный доступ через мостный уровень к элементам пользовательского интерфейса, поддерживающим только автоматизацию пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="31d94-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="31d94-112">Дополнительные сведения см. [в приложении ж: Active Accessibility Bridge to Automation UI](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="31d94-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="31d94-113">Дополнительные сведения о сходствах и различиях между Microsoft Active Accessibility и автоматизацией пользовательского интерфейса см. в [статье сравнение microsoft Active Accessibility и модели автоматизации пользовательского интерфейса](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="31d94-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31d94-114">См. также</span><span class="sxs-lookup"><span data-stu-id="31d94-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="31d94-115">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="31d94-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="31d94-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="31d94-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="31d94-117">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="31d94-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




