---
description: 'Функции Windows API, управляющие символами, обычно реализуются в одном из трех форматов:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Юникод в Windows API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683839"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="8d711-103">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="8d711-103">Unicode in the Windows API</span></span>

<span data-ttu-id="8d711-104">Функции Windows API, управляющие символами, обычно реализуются в одном из трех форматов:</span><span class="sxs-lookup"><span data-stu-id="8d711-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="8d711-105">Универсальная версия, которая может быть скомпилирована либо для кодовых страниц Windows, либо для Юникода</span><span class="sxs-lookup"><span data-stu-id="8d711-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="8d711-106">Версия [кодовой страницы Windows](code-pages.md) с буквой "A", используемой для обозначения "ANSI"</span><span class="sxs-lookup"><span data-stu-id="8d711-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="8d711-107">Версия в [Юникоде](unicode.md) с буквой "W", используемой для обозначения "Wide"</span><span class="sxs-lookup"><span data-stu-id="8d711-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="8d711-108">Некоторые новые функции поддерживают только версии Юникода.</span><span class="sxs-lookup"><span data-stu-id="8d711-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="8d711-109">Дополнительные сведения см. в разделе [соглашения для прототипов функций](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="8d711-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="8d711-110">В следующих разделах рассматриваются типы данных в Юникоде и их использование в функциях и сообщениях. использование ресурсов, имен файлов и аргументов командной строки; методы преобразования между различными типами строк.</span><span class="sxs-lookup"><span data-stu-id="8d711-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="8d711-111">Автоматическое преобразование сообщений</span><span class="sxs-lookup"><span data-stu-id="8d711-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="8d711-112">Кодировки, используемые в именах файлов</span><span class="sxs-lookup"><span data-stu-id="8d711-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="8d711-113">Аргументы командной строки</span><span class="sxs-lookup"><span data-stu-id="8d711-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="8d711-114">Правила обозначения прототипов функций</span><span class="sxs-lookup"><span data-stu-id="8d711-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="8d711-115">Стандартные функции C</span><span class="sxs-lookup"><span data-stu-id="8d711-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="8d711-116">Различия строковых функций</span><span class="sxs-lookup"><span data-stu-id="8d711-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="8d711-117">Преобразование между строковыми типами</span><span class="sxs-lookup"><span data-stu-id="8d711-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   <span data-ttu-id="8d711-118">[Windows Data Types for Strings](windows-data-types-for-strings.md) (Типы данных Windows для работы со строками)</span><span class="sxs-lookup"><span data-stu-id="8d711-118">[Windows Data Types for Strings](windows-data-types-for-strings.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d711-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8d711-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d711-120">О кодировке Юникод и кодировке</span><span class="sxs-lookup"><span data-stu-id="8d711-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



