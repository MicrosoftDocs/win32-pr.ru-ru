---
title: LANGUAGE, инструкция
description: Определяет язык для всех ресурсов вплоть до инструкции следующего языка или до конца файла.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Меню инструкций языка и другие ресурсы
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533167"
---
# <a name="language-statement"></a><span data-ttu-id="9a1be-104">LANGUAGE, инструкция</span><span class="sxs-lookup"><span data-stu-id="9a1be-104">LANGUAGE statement</span></span>

<span data-ttu-id="9a1be-105">Определяет язык для всех ресурсов вплоть до инструкции следующего **языка** или до конца файла.</span><span class="sxs-lookup"><span data-stu-id="9a1be-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="9a1be-106">Если оператор **Language** появляется перед началом тела определения ресурса [**ускорителей**](accelerators-resource.md), [**диаложекс**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)или [**STRINGTABLE**](stringtable-resource.md) , указанный язык применяется только к этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9a1be-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="9a1be-107"><span id="language"></span><span id="LANGUAGE"></span>*языке*</span><span class="sxs-lookup"><span data-stu-id="9a1be-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="9a1be-108">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="9a1be-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9a1be-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*вариантом*</span><span class="sxs-lookup"><span data-stu-id="9a1be-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="9a1be-110">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="9a1be-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="9a1be-111">Дополнительные сведения см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="9a1be-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a1be-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a1be-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1be-113">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="9a1be-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="9a1be-114">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="9a1be-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="9a1be-115">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="9a1be-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="9a1be-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="9a1be-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="9a1be-117">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="9a1be-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="9a1be-118">**Версия**</span><span class="sxs-lookup"><span data-stu-id="9a1be-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 