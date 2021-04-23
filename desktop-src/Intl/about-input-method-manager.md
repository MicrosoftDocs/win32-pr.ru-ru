---
description: Использование функций IMM в приложении, поддерживающем IME, позволяет избавляет пользователей от необходимости помнить все возможные символьные значения.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: О диспетчере методов ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683740"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="44727-103">О диспетчере методов ввода</span><span class="sxs-lookup"><span data-stu-id="44727-103">About Input Method Manager</span></span>

<span data-ttu-id="44727-104">Использование функций IMM в приложении, поддерживающем IME, позволяет избавляет пользователей от необходимости помнить все возможные символьные значения.</span><span class="sxs-lookup"><span data-stu-id="44727-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="44727-105">Вместо этого он позволяет редактору IME отслеживать нажатия клавиш пользователя, предвидит символы, которые может потребоваться пользователю, и предоставляет список потенциальных символов, из которых можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="44727-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="44727-106">IMM выполняет аналогичные операции с [платформой текстовых служб](../tsf/text-services-framework.md), используемыми приложениями, взаимодействующими с текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="44727-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="44727-107">По умолчанию IMM предоставляет окно IME, в котором пользователь вводит нажатия клавиш и представления и выбирает кандидатов.</span><span class="sxs-lookup"><span data-stu-id="44727-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="44727-108">Приложения могут использовать функции и сообщения IMM для создания собственных окон IME и управления ими, предоставляя пользовательский интерфейс при использовании возможностей преобразования IME.</span><span class="sxs-lookup"><span data-stu-id="44727-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="44727-109">Модуль IMM включен только в локализованных операционных системах Windows для восточноазиатских языков (китайского, японского, корейского).</span><span class="sxs-lookup"><span data-stu-id="44727-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="44727-110">В этих системах приложение вызывает [жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) с SM дбксенаблед, \_ чтобы определить, включен ли IMM.</span><span class="sxs-lookup"><span data-stu-id="44727-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="44727-111">**Windows 2000:** Полнофункциональная поддержка IMM предоставляется во всех локализованных версиях языка.</span><span class="sxs-lookup"><span data-stu-id="44727-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="44727-112">Однако IMM включается, только если установлен Азиатский языковой пакет.</span><span class="sxs-lookup"><span data-stu-id="44727-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="44727-113">Приложение, поддерживающее IME, может вызвать [жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) с SM \_ имменаблед, чтобы определить, включен ли IMM.</span><span class="sxs-lookup"><span data-stu-id="44727-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="44727-114">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="44727-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="44727-115">Списки кандидатов</span><span class="sxs-lookup"><span data-stu-id="44727-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="44727-116">Строка композиции</span><span class="sxs-lookup"><span data-stu-id="44727-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="44727-117">Хекстауникоде IME</span><span class="sxs-lookup"><span data-stu-id="44727-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="44727-118">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="44727-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="44727-119">Сообщения IME</span><span class="sxs-lookup"><span data-stu-id="44727-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="44727-120">Класс окна IME</span><span class="sxs-lookup"><span data-stu-id="44727-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="44727-121">Контекст ввода</span><span class="sxs-lookup"><span data-stu-id="44727-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="44727-122">Окна состояния, композиции и кандидатов</span><span class="sxs-lookup"><span data-stu-id="44727-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
