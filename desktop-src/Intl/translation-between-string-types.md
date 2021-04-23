---
description: Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Преобразование между строковыми типами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683516"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="28e73-103">Преобразование между строковыми типами</span><span class="sxs-lookup"><span data-stu-id="28e73-103">Translation Between String Types</span></span>

<span data-ttu-id="28e73-104">Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.</span><span class="sxs-lookup"><span data-stu-id="28e73-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="28e73-105">Функция</span><span class="sxs-lookup"><span data-stu-id="28e73-105">Function</span></span>                                           | <span data-ttu-id="28e73-106">Описание</span><span class="sxs-lookup"><span data-stu-id="28e73-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="28e73-107">**FoldString**</span><span class="sxs-lookup"><span data-stu-id="28e73-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="28e73-108">Преобразует одну строку символов в другую.</span><span class="sxs-lookup"><span data-stu-id="28e73-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="28e73-109">**LCMapString завершилось ошибкой**</span><span class="sxs-lookup"><span data-stu-id="28e73-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="28e73-110">Сопоставляет строку символов по языку и региональным параметрам.</span><span class="sxs-lookup"><span data-stu-id="28e73-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="28e73-111">**тауникоде**</span><span class="sxs-lookup"><span data-stu-id="28e73-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="28e73-112">Преобразует виртуальный код ключа в символ Юникода.</span><span class="sxs-lookup"><span data-stu-id="28e73-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="28e73-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="28e73-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="28e73-114">Сопоставляет многобайтовую строку со строкой в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="28e73-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="28e73-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="28e73-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="28e73-116">Сопоставляет строку Юникода с многобайтовой строкой.</span><span class="sxs-lookup"><span data-stu-id="28e73-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="28e73-117">Функции [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) и [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) особенно полезны для приложений, поддерживающих несколько строковых типов.</span><span class="sxs-lookup"><span data-stu-id="28e73-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="28e73-118">В ANSI C также определяются функции преобразования **wcstombs** и **функции mbstowcs**, но они могут преобразовывать только в набор символов, поддерживаемый стандартной библиотекой C.</span><span class="sxs-lookup"><span data-stu-id="28e73-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28e73-119">См. также</span><span class="sxs-lookup"><span data-stu-id="28e73-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28e73-120">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="28e73-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
