---
description: Большинство строковых операций может использовать одну и ту же логику для Юникода и для кодовых страниц Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Типы данных Windows для работы со строками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081614"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="30e3a-103">Типы данных Windows для работы со строками</span><span class="sxs-lookup"><span data-stu-id="30e3a-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="30e3a-104">Большинство строковых операций может использовать одну и ту же логику для [Юникода](unicode.md) и для [кодовых страниц Windows](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="30e3a-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="30e3a-105">Единственное отличие состоит в том, что базовая единица операции — 16-разрядный символ (также известный как широкий символ) для Юникода и 8-разрядный символ для кодовых страниц Windows.</span><span class="sxs-lookup"><span data-stu-id="30e3a-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="30e3a-106">Файлы заголовков Windows предоставляют несколько определений типов, которые упрощают создание источников, которые можно скомпилировать для Юникода или для кодовых страниц Windows.</span><span class="sxs-lookup"><span data-stu-id="30e3a-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="30e3a-107">Windows поддерживает три набора символьных и строковых типов данных: набор определений универсальных типов, которые могут быть скомпилированы для кодовых страниц в Юникоде или Windows, и два набора определений определенных типов.</span><span class="sxs-lookup"><span data-stu-id="30e3a-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="30e3a-108">Один набор определений определенных типов предназначен для использования в Юникоде, а другой — для использования с кодовыми страницами Windows.</span><span class="sxs-lookup"><span data-stu-id="30e3a-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="30e3a-109">Приложение, использующее универсальные типы данных, может быть скомпилировано для Юникода просто путем определения "UNICODE" перед инструкциями **\# include** для файлов заголовков или во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="30e3a-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="30e3a-110">Новые приложения Windows должны использовать Юникод, чтобы избежать несоответствий между различными кодовыми страницами и упростить локализацию.</span><span class="sxs-lookup"><span data-stu-id="30e3a-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="30e3a-111">Они должны быть написаны с универсальными типами данных и должны определять "UNICODE" для компиляции этих типов в типы Юникода.</span><span class="sxs-lookup"><span data-stu-id="30e3a-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="30e3a-112">В некоторых местах, где приложение должно работать с 8-разрядными символьными данными, оно может явно использовать типы для кодовых страниц Windows.</span><span class="sxs-lookup"><span data-stu-id="30e3a-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="30e3a-113">Возможность компилировать универсальные типы в типы для кодовых страниц Windows в основном существует для поддержки устаревших приложений.</span><span class="sxs-lookup"><span data-stu-id="30e3a-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="30e3a-114">Для компиляции кодовых страниц Windows приложение просто опускает определение Юникода.</span><span class="sxs-lookup"><span data-stu-id="30e3a-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="30e3a-115">В следующем примере показан метод, используемый в файлах заголовков Windows для определения трех наборов типов данных.</span><span class="sxs-lookup"><span data-stu-id="30e3a-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="30e3a-116">Сведения о реализации см. в файле заголовка WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="30e3a-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="30e3a-117">Буква "T" в определении типа, например TCHAR или LPTSTR, обозначает универсальный тип, который может быть скомпилирован для кодовых страниц Windows или Юникода.</span><span class="sxs-lookup"><span data-stu-id="30e3a-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="30e3a-118">Буква "W" в определении типа, например WCHAR или LPWSTR, обозначает тип Юникода.</span><span class="sxs-lookup"><span data-stu-id="30e3a-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="30e3a-119">Поскольку кодовые страницы Windows имеют более старую форму, они имеют простые определения типов, такие как CHAR и LPSTR.</span><span class="sxs-lookup"><span data-stu-id="30e3a-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="30e3a-120">Полное описание типов данных в Windows см. в разделе [типы данных Windows](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="30e3a-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30e3a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="30e3a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e3a-122">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="30e3a-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
