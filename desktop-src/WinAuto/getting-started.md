---
title: Начало работы (Microsoft Active Accessibility)
description: Microsoft Active Accessibility — это набор интерфейсов COM и интерфейсов API, обеспечивающих надежный способ предоставления и получения сведений об элементах пользовательского интерфейса и веб-содержимом на основе Microsoft Windows.
ms.assetid: 13148049-dbb0-4529-b1d7-0c41ebeb7543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8e84f6e647868b23e845522c137e6cfb1b9dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691748"
---
# <a name="getting-started-microsoft-active-accessibility"></a><span data-ttu-id="a539e-103">Начало работы (Microsoft Active Accessibility)</span><span class="sxs-lookup"><span data-stu-id="a539e-103">Getting Started (Microsoft Active Accessibility)</span></span>

<span data-ttu-id="a539e-104">Microsoft Active Accessibility — это набор интерфейсов COM и интерфейсов API, обеспечивающих надежный способ предоставления и получения сведений об элементах пользовательского интерфейса и веб-содержимом на основе Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a539e-104">Microsoft Active Accessibility is a set of Component Object Model (COM) interfaces and API elements that provide a reliable way to expose and collect information about Microsoft Windows-based UI elements and web content.</span></span> <span data-ttu-id="a539e-105">С помощью этой информации поставщики вспомогательных технологий могут представлять пользовательский интерфейс в альтернативных форматах, таких как речь или Брайля, а приложения голосовой команды и элементы управления могут удаленно управлять интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="a539e-105">Using this information, assistive technology vendors can represent the UI in alternative formats, such as speech or Braille, and voice command and control applications can remotely manipulate the interface.</span></span> <span data-ttu-id="a539e-106">Microsoft Active Accessibility полагается на технологию Windows и может использоваться в сочетании только с элементами управления на основе Windows и другими приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="a539e-106">Microsoft Active Accessibility relies on Windows technology and can be used in conjunction only with Windows-based controls and other Windows applications.</span></span>

<span data-ttu-id="a539e-107">Эта документация организована в соответствии с потребностями разработчиков, которые впервые знакомы с, а также с Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="a539e-107">This documentation is organized to meet the needs of developers new to, as well as those familiar with, Microsoft Active Accessibility.</span></span> <span data-ttu-id="a539e-108">Основные разделы документации описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="a539e-108">The major sections of the documentation are described below:</span></span>



|                                                        |                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a539e-109">Технический обзор</span><span class="sxs-lookup"><span data-stu-id="a539e-109">Technical Overview</span></span>](technical-overview.md)           | <span data-ttu-id="a539e-110">Общие сведения о Active Accessibility Майкрософт и общих рекомендациях для разработчиков клиентов и серверов Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="a539e-110">Overview of Microsoft Active Accessibility and general guidelines for Microsoft Active Accessibility client and server developers.</span></span>                                |
| [<span data-ttu-id="a539e-111">Рекомендации для разработчиков C/C++</span><span class="sxs-lookup"><span data-stu-id="a539e-111">C/C++ Developer's Guide</span></span>](c-c---developer-s-guide.md) | <span data-ttu-id="a539e-112">Подробные сведения о ключевых элементах и концепциях API приложения Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="a539e-112">In-depth information about the key Microsoft Active Accessibility application API elements and concepts.</span></span> <span data-ttu-id="a539e-113">Использует термины и примеры, знакомые разработчикам C или C++.</span><span class="sxs-lookup"><span data-stu-id="a539e-113">Uses terms and examples familiar to C or C++ developers.</span></span> |
| [<span data-ttu-id="a539e-114">Справочник по C/C++</span><span class="sxs-lookup"><span data-stu-id="a539e-114">C/C++ Reference</span></span>](c-c---reference.md)                 | <span data-ttu-id="a539e-115">Исчерпывающий Справочник по всем интерфейсам Active Accessibility Майкрософт, функциям, типам данных, структурам данных и сообщениям.</span><span class="sxs-lookup"><span data-stu-id="a539e-115">A comprehensive reference for all the Microsoft Active Accessibility interfaces, functions , data types, data structures, and messages.</span></span>                           |
| [<span data-ttu-id="a539e-116">Приложения</span><span class="sxs-lookup"><span data-stu-id="a539e-116">Appendixes</span></span>](appendixes.md)                           | <span data-ttu-id="a539e-117">Дополнительные справочные материалы для разработчиков клиентов и серверов Microsoft Active Accessibility и Microsoft Visual Басикдевелоперс.</span><span class="sxs-lookup"><span data-stu-id="a539e-117">Additional reference material for Microsoft Active Accessibility client and server developers and Microsoft Visual Basicdevelopers.</span></span>                               |



 

## <a name="in-this-section"></a><span data-ttu-id="a539e-118">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="a539e-118">In this section</span></span>

-   [<span data-ttu-id="a539e-119">Компоненты Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="a539e-119">Active Accessibility Components</span></span>](sdk-components.md)
-   [<span data-ttu-id="a539e-120">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="a539e-120">Supported Platforms</span></span>](supported-platforms.md)
-   [<span data-ttu-id="a539e-121">Active Accessibility и автоматизация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a539e-121">Active Accessibility and UI Automation</span></span>](active-accessibility-and-ui-automation.md)

 

 




