---
description: Кодовая страница — это внутренняя таблица, используемая операционной системой для отображения символов (букв, цифр и знаков препинания) в номере символа.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Проверка кодовой страницы базы данных установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662903"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="22b90-103">Проверка кодовой страницы базы данных установки</span><span class="sxs-lookup"><span data-stu-id="22b90-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="22b90-104">*Кодовая страница* — это внутренняя таблица, используемая операционной системой для отображения символов (букв, цифр и знаков препинания) в номере символа.</span><span class="sxs-lookup"><span data-stu-id="22b90-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="22b90-105">Различные кодовые страницы обеспечивают поддержку наборов символов, используемых в разных странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="22b90-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="22b90-106">Кодовые страницы упоминаются по числу; Например, кодовая страница 932 представляет собой японскую кодировку, а кодовая страница 950 — одну из китайских кодировок.</span><span class="sxs-lookup"><span data-stu-id="22b90-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="22b90-107">Список кодовых страниц ASCII см. [в разделе Локализация таблиц ошибок и актионтекст](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="22b90-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="22b90-108">Та же кодовая страница ASCII, 1252, может использоваться для английского и французского языков.</span><span class="sxs-lookup"><span data-stu-id="22b90-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="22b90-109">Поэтому кодовую страницу MNP2000.msi базы данных (на английском языке) не нужно сбрасывать, чтобы изменить установку на французский.</span><span class="sxs-lookup"><span data-stu-id="22b90-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="22b90-110">Дополнительные сведения о настройке кодовой страницы см. в разделе [Обработка кодовых страниц (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="22b90-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="22b90-111">Продолжить</span><span class="sxs-lookup"><span data-stu-id="22b90-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



