---
description: Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651113"
---
# <a name="script_string_analysis"></a><span data-ttu-id="504a1-103">\_анализ строки скрипта \_</span><span class="sxs-lookup"><span data-stu-id="504a1-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="504a1-104">Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.</span><span class="sxs-lookup"><span data-stu-id="504a1-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="504a1-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="504a1-105">Remarks</span></span>

<span data-ttu-id="504a1-106">Это непрозрачная структура, которая выделяется динамически и извлекается с помощью [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span><span class="sxs-lookup"><span data-stu-id="504a1-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="504a1-107">Он необходим и для всех остальных функций \*\* \* скриптстринг\* _.</span><span class="sxs-lookup"><span data-stu-id="504a1-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="504a1-108">Так как анализ может быть большим, важно, чтобы приложение вызывало [_ *скриптстрингфри* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) сразу после завершения строки.</span><span class="sxs-lookup"><span data-stu-id="504a1-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="504a1-109">Требования</span><span class="sxs-lookup"><span data-stu-id="504a1-109">Requirements</span></span>



| <span data-ttu-id="504a1-110">Требование</span><span class="sxs-lookup"><span data-stu-id="504a1-110">Requirement</span></span> | <span data-ttu-id="504a1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="504a1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="504a1-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="504a1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="504a1-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="504a1-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="504a1-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="504a1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="504a1-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="504a1-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="504a1-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="504a1-116">Redistributable</span></span><br/>          | <span data-ttu-id="504a1-117">Internet Explorer 5 или более поздняя версия — Windows Me/98/95</span><span class="sxs-lookup"><span data-stu-id="504a1-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="504a1-118">Header</span><span class="sxs-lookup"><span data-stu-id="504a1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="504a1-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="504a1-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="504a1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="504a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504a1-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="504a1-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="504a1-122">Структуры Uniscribe</span><span class="sxs-lookup"><span data-stu-id="504a1-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="504a1-123">**скриптстринганалисе**</span><span class="sxs-lookup"><span data-stu-id="504a1-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="504a1-124">**скриптстрингфри**</span><span class="sxs-lookup"><span data-stu-id="504a1-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




