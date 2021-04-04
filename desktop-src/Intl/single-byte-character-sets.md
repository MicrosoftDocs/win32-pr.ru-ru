---
description: Однобайтовая кодировка (SBCS) — это сопоставление 256 отдельных символов с их кодовыми значениями, реализованными в виде кодовой страницы.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Однобайтовые кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999601"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="2ada4-103">Однобайтовые кодировки</span><span class="sxs-lookup"><span data-stu-id="2ada4-103">Single-byte Character Sets</span></span>

<span data-ttu-id="2ada4-104">Однобайтовая кодировка (SBCS) — это сопоставление 256 отдельных символов с их кодовыми значениями, реализованными в виде кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="2ada4-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="2ada4-105">SBCS может соответствовать кодовой странице Windows или кодовой странице OEM.</span><span class="sxs-lookup"><span data-stu-id="2ada4-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="2ada4-106">Однобайтовая кодовая страница может также включать немашинную кодовую страницу, например кодовую страницу EBCDIC.</span><span class="sxs-lookup"><span data-stu-id="2ada4-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="2ada4-107">Определения этих кодовых страниц см. в разделе [кодовые страницы](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="2ada4-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ada4-108">Новые приложения Windows должны использовать [Юникод](unicode.md) , чтобы избежать несоответствий между различными кодовыми страницами и простотой локализации.</span><span class="sxs-lookup"><span data-stu-id="2ada4-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="2ada4-109">Однако для некоторых устаревших протоколов требуется использовать SBCS.</span><span class="sxs-lookup"><span data-stu-id="2ada4-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="2ada4-110">Каждая Однобайтовая кодовая страница поддерживает разные символы, но ни одна страница не поддерживает полный набор символов, предоставляемых в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="2ada4-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="2ada4-111">Каждая Однобайтовая кодовая страница поддерживает разные подмножества, которые кодируются по-разному.</span><span class="sxs-lookup"><span data-stu-id="2ada4-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="2ada4-112">Данные, преобразованные из одной однобайтовой кодовой страницы в другую, подвергаются повреждению, так как одно и то же значение данных на разных кодовых страницах может кодировать другой символ.</span><span class="sxs-lookup"><span data-stu-id="2ada4-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="2ada4-113">Данные, преобразованные из Юникода в SBCS, подвергаются потери данных, так как данная кодовая страница может не представлять каждый символ, используемый в определенных данных в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="2ada4-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="2ada4-114">Приложения используют однобайтовые кодовые страницы Windows с версиями функций Windows "A".</span><span class="sxs-lookup"><span data-stu-id="2ada4-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="2ada4-115">См. раздел [соглашения для прототипов функций](conventions-for-function-prototypes.md) и [кодовых страниц](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="2ada4-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="2ada4-116">Для поиска однобайтовой кодовой страницы приложение может использовать функцию [**жеткпинфо**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) или [**жеткпинфоекс**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="2ada4-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="2ada4-117">Кроме того, приложение может использовать функции [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) и [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) для СОПОСТАВЛЕНИЯ строк Юникода и SBCS.</span><span class="sxs-lookup"><span data-stu-id="2ada4-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ada4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2ada4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ada4-119">Кодировки</span><span class="sxs-lookup"><span data-stu-id="2ada4-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="2ada4-120">Двухбайтовые кодировки</span><span class="sxs-lookup"><span data-stu-id="2ada4-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



