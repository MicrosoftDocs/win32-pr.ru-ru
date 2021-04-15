---
description: Идентификатор языка — это стандартное Международный цифровой сокращенный номер языка в стране или географическом регионе.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Идентификаторы языка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662501"
---
# <a name="language-identifiers"></a><span data-ttu-id="7bb84-103">Идентификаторы языка</span><span class="sxs-lookup"><span data-stu-id="7bb84-103">Language Identifiers</span></span>

<span data-ttu-id="7bb84-104">Идентификатор языка — это стандартное Международный цифровой сокращенный номер [языка](locales-and-languages.md) в стране или географическом регионе.</span><span class="sxs-lookup"><span data-stu-id="7bb84-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="7bb84-105">Каждый язык имеет уникальный идентификатор языка (тип данных LANGID), 16-разрядное значение, состоящее из основного идентификатора языка и идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="7bb84-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="7bb84-106">Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](language-identifier-constants-and-strings.md).</span><span class="sxs-lookup"><span data-stu-id="7bb84-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="7bb84-107">Идентификатор языка создается с помощью макроса [**макелангид**](/windows/desktop/api/Winnt/nf-winnt-makelangid) .</span><span class="sxs-lookup"><span data-stu-id="7bb84-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="7bb84-108">На следующем рисунке показан формат битов в идентификаторе языка.</span><span class="sxs-lookup"><span data-stu-id="7bb84-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="7bb84-109">Ниже приведены предопределенные идентификаторы языка.</span><span class="sxs-lookup"><span data-stu-id="7bb84-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="7bb84-110">\_ \_ по умолчанию используется язык lang.</span><span class="sxs-lookup"><span data-stu-id="7bb84-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="7bb84-111">Язык операционной системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bb84-111">The operating system default language.</span></span>
-   <span data-ttu-id="7bb84-112">\_пользователь lang \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bb84-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="7bb84-113">Язык текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="7bb84-113">The language of the current user.</span></span>

<span data-ttu-id="7bb84-114">Приложение может извлекать текущие идентификаторы языков с помощью функций [многоязыкового интерфейса пользователя](multilingual-user-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb84-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bb84-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7bb84-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb84-116">Языковые стандарты и языки</span><span class="sxs-lookup"><span data-stu-id="7bb84-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="7bb84-117">Константы и строки идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="7bb84-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="7bb84-118">Многоязыковой интерфейс пользователя</span><span class="sxs-lookup"><span data-stu-id="7bb84-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="7bb84-119">**макелангид**</span><span class="sxs-lookup"><span data-stu-id="7bb84-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



