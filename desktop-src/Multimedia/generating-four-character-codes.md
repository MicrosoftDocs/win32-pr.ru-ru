---
title: Создание кодов Four-Character
description: Создание кодов Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- Ввод-вывод файлов мультимедиа, коды из четырех символов
- Ввод-вывод в файл, коды из четырех символов
- Ввод и вывод (I/O), коды из четырех символов
- Ввод-вывод (ввод и вывод), коды из четырех символов
- коды из четырех символов
- Функция Ммиострингтофауркк
- макрос Ммиофауркк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789991"
---
# <a name="generating-four-character-codes"></a><span data-ttu-id="e425d-110">Создание кодов Four-Character</span><span class="sxs-lookup"><span data-stu-id="e425d-110">Generating Four-Character Codes</span></span>

<span data-ttu-id="e425d-111">Для создания четырех кодов символов можно использовать макрос [**ммиофауркк**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) или функцию [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) .</span><span class="sxs-lookup"><span data-stu-id="e425d-111">You can use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro or the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function to generate four-character codes.</span></span> <span data-ttu-id="e425d-112">В следующем примере используется **ммиофауркк** для создания кода с четырьмя символами для "Wave".</span><span class="sxs-lookup"><span data-stu-id="e425d-112">The following example uses **mmioFOURCC** to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



<span data-ttu-id="e425d-113">В следующем примере используется [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) для создания кода с четырьмя символами для "Wave".</span><span class="sxs-lookup"><span data-stu-id="e425d-113">The following example uses [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



<span data-ttu-id="e425d-114">Второй параметр в [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) указывает флаги для преобразования строки в код из четырех символов.</span><span class="sxs-lookup"><span data-stu-id="e425d-114">The second parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifies flags for converting the string to a four-character code.</span></span> <span data-ttu-id="e425d-115">При указании \_ флага MMIO **ммиострингтофауркк** преобразует все буквы в строке в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="e425d-115">If you specify the MMIO\_TOUPPER flag, **mmioStringToFOURCC** converts all alphabetic characters in the string to uppercase.</span></span> <span data-ttu-id="e425d-116">Это полезно, если необходимо указать код из четырех символов для идентификации пользовательской процедуры ввода-вывода, так как в четырех кодах символов, идентифицирующих имена файлов, должно быть задано все прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="e425d-116">This is useful when you need to specify a four-character code to identify a custom I/O procedure because four-character codes identifying file-extension names must be all uppercase.</span></span>

 

 