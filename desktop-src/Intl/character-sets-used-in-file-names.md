---
description: NTFS сохраняет имена файлов в Юникоде. Напротив, в старых файловых системах FAT12, FAT16 и FAT32 используется набор символов OEM. Для получения дополнительной информации см. Кодовые страницы.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Кодировки, используемые в именах файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910723"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="804d2-105">Кодировки, используемые в именах файлов</span><span class="sxs-lookup"><span data-stu-id="804d2-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="804d2-106">NTFS сохраняет имена файлов в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="804d2-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="804d2-107">Напротив, в старых файловых системах FAT12, FAT16 и FAT32 используется набор символов OEM.</span><span class="sxs-lookup"><span data-stu-id="804d2-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="804d2-108">Дополнительные сведения см. в разделе [Кодовые страницы](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="804d2-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="804d2-109">Приложения, не поддерживающие Юникод, которые создают файлы FAT, иногда должны использовать стандартные функции преобразования библиотеки времени выполнения C для преобразования между набором символов кодовой страницы Windows и кодировкой кодовой страницы OEM.</span><span class="sxs-lookup"><span data-stu-id="804d2-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="804d2-110">При реализации функций файловой системы в Юникоде нет необходимости выполнять такие переводы.</span><span class="sxs-lookup"><span data-stu-id="804d2-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="804d2-111">Приложение может использовать универсальные строковые типы, как описано в разделе [типы данных Windows для строк](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="804d2-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="804d2-112">Приложение также может использовать прототипы универсальных функций, используя методы, описанные в разделе [соглашения о прототипах функций](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="804d2-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="804d2-113">Для универсальных строковых типов или прототипов универсальных функций приложение может использовать один исходный файл для компиляции либо версии Юникода, либо не поддерживающей Юникод.</span><span class="sxs-lookup"><span data-stu-id="804d2-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="804d2-114">Чтобы это сделать, приложение предоставляет макросы для функций, которые не вызываются при компиляции для Юникода.</span><span class="sxs-lookup"><span data-stu-id="804d2-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="804d2-115">В файловых системах NTFS и FAT специальные символы имени файла: " \\ ", "/", ".", "?" и " \* ".</span><span class="sxs-lookup"><span data-stu-id="804d2-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="804d2-116">На кодовых страницах OEM эти специальные символы находятся в диапазоне ASCII символов (от 0x00 до 0x7F).</span><span class="sxs-lookup"><span data-stu-id="804d2-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="804d2-117">Их эквиваленты в Юникоде представляют собой одинаковые значения в 2-байтовой форме, символ 0x0000 через 0x007F.</span><span class="sxs-lookup"><span data-stu-id="804d2-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="804d2-118">Кодовая страница Windows и наборы символов кодовых страниц OEM, используемые в операционных системах на японском языке, содержат символ [¥) вместо обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="804d2-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="804d2-119">Таким словами, символ «символы» является запрещенным для файловых систем NTFS и FAT.</span><span class="sxs-lookup"><span data-stu-id="804d2-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="804d2-120">При сопоставлении Юникода с кодовой страницей на японском языке [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) и другие функции преобразования сопоставляют обратную косую черту (u + 005C) и Стандартный символ Юникода в Юникоде (u + 00A5) этому же символу.</span><span class="sxs-lookup"><span data-stu-id="804d2-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="804d2-121">По соображениям безопасности приложения обычно не должны допускать символ U + 00A5 в строке Юникода, которую можно преобразовать для использования в качестве имени файла FAT.</span><span class="sxs-lookup"><span data-stu-id="804d2-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="804d2-122">Дополнительные сведения см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="804d2-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="804d2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="804d2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="804d2-124">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="804d2-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="804d2-125">Вопросы безопасности: международные функции</span><span class="sxs-lookup"><span data-stu-id="804d2-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



