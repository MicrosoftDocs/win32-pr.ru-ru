---
description: Консольное приложение MUI может поддерживать параметры системы или параметры приложения для языков пользовательского интерфейса. В этом разделе обсуждается фильтрация языков для этого типа приложения.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Фильтрация языков в консольном приложении MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910120"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="9d15f-104">Фильтрация языков в консольном приложении MUI</span><span class="sxs-lookup"><span data-stu-id="9d15f-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="9d15f-105">Консольное приложение MUI может поддерживать параметры системы или параметры приложения для языков пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9d15f-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="9d15f-106">В этом разделе обсуждается фильтрация языков для этого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9d15f-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="9d15f-107">Ограничить отображаемые языки</span><span class="sxs-lookup"><span data-stu-id="9d15f-107">Limit the Languages to Display</span></span>

<span data-ttu-id="9d15f-108">В отличие от графического окна Консоль Windows не может отображать [сложные наборы символов](uniscribe-glossary.md), такие как арабский, иврит, Персидский, хинди, урду, тайский и многие другие.</span><span class="sxs-lookup"><span data-stu-id="9d15f-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="9d15f-109">Поэтому консоль не может отображать многие языки пользовательского интерфейса при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="9d15f-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="9d15f-110">Консоль может отображать только символы из одной [кодовой страницы OEM](code-pages.md) , связанной с текущим языком для приложений, не поддерживающих Юникод.</span><span class="sxs-lookup"><span data-stu-id="9d15f-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="9d15f-111">Для каждой кодовой страницы OEM консоль использует определенный шрифт, и это может привести к неполному охвату этой кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="9d15f-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="9d15f-112">Эти ограничения, связанные с консолью, уменьшают количество языков пользовательского интерфейса, которые консоль может отображать на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9d15f-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="9d15f-113">Например, если текущий язык для приложений, не поддерживающих Юникод, является японским и пользователь пытается отобразить в консоли текст на немецком языке, символы с умлаутс отображаются неправильно.</span><span class="sxs-lookup"><span data-stu-id="9d15f-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="9d15f-114">Если текущий язык для приложений, не поддерживающих Юникод, является немецким и пользователь хочет отобразить на консоли текст на японском языке, результаты значительно хуже, а визуализация текста почти непонятная.</span><span class="sxs-lookup"><span data-stu-id="9d15f-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="9d15f-115">При предоставлении поддержки консоли для приложений MUI Помните, что консоль предоставляет только ограниченную поддержку [редакторов методов ввода](input-method-manager.md).</span><span class="sxs-lookup"><span data-stu-id="9d15f-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="9d15f-116">Установка языка для вывода консоли</span><span class="sxs-lookup"><span data-stu-id="9d15f-116">Set the Language for Console Output</span></span>

<span data-ttu-id="9d15f-117">В Windows Vista и более поздних версиях консольное приложение устанавливает язык, поддерживающий отображение консоли, вызывая [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="9d15f-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="9d15f-118">В этом вызове приложение передает \_ Фильтр консоли MUI \_ в параметре *DwFlags* и **значение NULL** для *пвсзлангуажесбуффер*.</span><span class="sxs-lookup"><span data-stu-id="9d15f-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="9d15f-119">Альтернативой является вызов [**сетсреадуилангуаже**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) с идентификатором языка 0.</span><span class="sxs-lookup"><span data-stu-id="9d15f-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="9d15f-120">Этот параметр приводит к тому, что функция выбирает язык, который наилучшим образом поддерживает отображение консоли.</span><span class="sxs-lookup"><span data-stu-id="9d15f-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="9d15f-121">В Windows XP приложение может установить язык только для вывода консоли, вызвав [**сетсреадуилангуаже**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) с идентификатором языка 0.</span><span class="sxs-lookup"><span data-stu-id="9d15f-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d15f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9d15f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d15f-123">Настройка языковых настроек приложения</span><span class="sxs-lookup"><span data-stu-id="9d15f-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
