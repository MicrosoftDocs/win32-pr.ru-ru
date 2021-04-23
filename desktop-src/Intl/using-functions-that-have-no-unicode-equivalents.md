---
description: Функции, которые не были реализованы в версии Юникода, обычно заменены более мощными или расширенными функциями, поддерживающими Юникод.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Использование функций, не имеющих эквивалентов в Юникоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272956"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="41e5a-103">Использование функций, не имеющих эквивалентов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="41e5a-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="41e5a-104">Функции, которые не были реализованы в версии [Юникода](unicode.md) , обычно заменены более мощными или расширенными функциями, поддерживающими Юникод.</span><span class="sxs-lookup"><span data-stu-id="41e5a-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="41e5a-105">Например, при переносе кода, который вызывает функцию [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , приложение может поддерживать Юникод с помощью функции [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="41e5a-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="41e5a-106">Если функция не имеет эквивалента в Юникоде, приложение может сопоставлять символы и из 8-разрядных наборов символов до и после вызова функции.</span><span class="sxs-lookup"><span data-stu-id="41e5a-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="41e5a-107">Например, функции форматирования чисел **atoi** и **Итоа** используют только цифры от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="41e5a-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="41e5a-108">Как правило, сопоставление Юникода с 8-разрядными символами приводит к утрате данных, но это можно избежать, сделав независимым от типа кода и сделав выражения условными.</span><span class="sxs-lookup"><span data-stu-id="41e5a-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="41e5a-109">Инструкции в следующем примере, написанные для 8-разрядных символов, зависят от типа и должны быть изменены для поддержки Юникода.</span><span class="sxs-lookup"><span data-stu-id="41e5a-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="41e5a-110">Эти инструкции можно переписывать следующим образом, чтобы сделать их независимыми от типов.</span><span class="sxs-lookup"><span data-stu-id="41e5a-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="41e5a-111">В этом примере Стандартная функция библиотеки C **wcstombs** преобразует Юникод в ASCII.</span><span class="sxs-lookup"><span data-stu-id="41e5a-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="41e5a-112">В этом примере используется тот факт, что цифры от 0 до 9 всегда могут быть преобразованы из Юникода в ASCII, даже если часть окружающего текста не может.</span><span class="sxs-lookup"><span data-stu-id="41e5a-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="41e5a-113">Функция **atoi** останавливается на любом символе, который не является цифрой.</span><span class="sxs-lookup"><span data-stu-id="41e5a-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="41e5a-114">Приложение может использовать функцию [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) национальных языков (NLS) для обработки текста, содержащего [собственные цифры](digit-shapes.md) , предоставленные для некоторых скриптов в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="41e5a-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="41e5a-115">Неправильное использование функции **wcstombs** может привести к нарушению безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="41e5a-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="41e5a-116">Убедитесь, что буфер приложения для строки 8-разрядных символов имеет размер не меньше 2 \* (*символьная \_ Длина* + 1), где *char \_ length* представляет длину строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="41e5a-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="41e5a-117">Это ограничение устанавливается потому, что с двухбайтовыми [наборами символов](double-byte-character-sets.md) (DBCS) каждый символ Юникода может быть сопоставлен с двумя последовательными 8-разрядными символами.</span><span class="sxs-lookup"><span data-stu-id="41e5a-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="41e5a-118">Если буфер не содержит всю строку, результирующая строка не завершается нулем, что приводит к угрозе безопасности.</span><span class="sxs-lookup"><span data-stu-id="41e5a-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="41e5a-119">Дополнительные сведения о безопасности приложений см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="41e5a-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="41e5a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="41e5a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e5a-121">Использование Юникода и кодировок</span><span class="sxs-lookup"><span data-stu-id="41e5a-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
