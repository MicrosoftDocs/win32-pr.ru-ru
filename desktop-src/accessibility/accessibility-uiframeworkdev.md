---
description: Обзор специальных возможностей Windows, которые можно включить в платформу пользовательского интерфейса.
title: Разработка платформ пользовательского интерфейса со специальными возможностями для Windows
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 9083bdb8b9c7ab9dd7dd30c675a72fafa4c065c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142646"
---
# <a name="developing-accessible-ui-frameworks-for-windows"></a><span data-ttu-id="9216d-103">Разработка платформ пользовательского интерфейса со специальными возможностями для Windows</span><span class="sxs-lookup"><span data-stu-id="9216d-103">Developing accessible UI frameworks for Windows</span></span>

<span data-ttu-id="9216d-104">Платформам пользовательского интерфейса, созданным для платформы Windows, должны поддерживаться специальные возможности, упрощающие работу с ограниченными возможностями, личными предпочтениями или конкретными стилями работы для успешного использования устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="9216d-104">To be usable by as many people as possible, UI frameworks built for the Windows platform should support accessibility features that make it easier for those with disabilities, personal preferences, or specific work styles to use their Windows devices successfully.</span></span>

<span data-ttu-id="9216d-105">В этом обзоре описывается создание платформы пользовательского интерфейса, которая поддерживает такие функции, как программный доступ и Автоматизация, Навигация с помощью клавиатуры и команды, параметры цвета и темы, а также Персонализация с помощью параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="9216d-105">This overview describes how to build a UI framework that supports features such as programmatic access and automation, keyboard navigation and commanding, color and theme options, and personalization through user settings.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9216d-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="9216d-106">In this section</span></span>

- [<span data-ttu-id="9216d-107">Модель автоматизации пользовательского интерфейса для Win32</span><span class="sxs-lookup"><span data-stu-id="9216d-107">UI Automation for Win32</span></span>](/windows/desktop/winauto/entry-uiauto-win32)
- [<span data-ttu-id="9216d-108">Специальные возможности клавиатуры</span><span class="sxs-lookup"><span data-stu-id="9216d-108">Keyboard accessibility</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
- [<span data-ttu-id="9216d-109">Соблюдение высокая контрастность</span><span class="sxs-lookup"><span data-stu-id="9216d-109">Respecting High Contrast</span></span>](/windows/desktop/w8cookbook/high-contrast-mode)
- [<span data-ttu-id="9216d-110">Параметры пользователя</span><span class="sxs-lookup"><span data-stu-id="9216d-110">User settings</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
- [<span data-ttu-id="9216d-111">Запись блога о параметрах пользователя</span><span class="sxs-lookup"><span data-stu-id="9216d-111">User settings blog post</span></span>](https://devblogs.microsoft.com/oldnewthing/?p=36243)

<span data-ttu-id="9216d-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="9216d-112">Samples</span></span>

- [<span data-ttu-id="9216d-113">Пример реализации платформы WPF модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9216d-113">UI Automation WPF Framework Implementation sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Accessibility)
- <span data-ttu-id="9216d-114">[Пример контрастности и параметров пользовательского интерфейса](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="9216d-114">[UI contrast and settings sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span></span>
