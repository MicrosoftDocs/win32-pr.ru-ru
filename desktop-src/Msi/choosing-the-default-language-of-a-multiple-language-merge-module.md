---
description: Язык по умолчанию для модуля слияния — это язык, указанный в таблице ModuleSignature модуля перед применением преобразований языка. Это также первый язык, указанный в свойстве сводка шаблона.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Выбор языка по умолчанию для модуля слияния с несколькими языками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909035"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="f303d-104">Выбор языка по умолчанию для модуля слияния с несколькими языками</span><span class="sxs-lookup"><span data-stu-id="f303d-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="f303d-105">Язык по умолчанию для модуля слияния — это язык, указанный в [таблице ModuleSignature](modulesignature-table.md) модуля перед применением преобразований языка.</span><span class="sxs-lookup"><span data-stu-id="f303d-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="f303d-106">Это также первый язык, указанный в свойстве [**Сводка шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="f303d-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="f303d-107">Язык по умолчанию для модуля должен быть одним из наиболее конкретных поддерживаемых языков, так как язык по умолчанию всегда проверяется первым, и если он соответствует требуемому языку, он используется, даже если другой язык лучше соответствует.</span><span class="sxs-lookup"><span data-stu-id="f303d-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="f303d-108">Например, если модуль поддерживает 1033 и 0, то 1033 должен быть языком по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f303d-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="f303d-109">Если значение по умолчанию равно 0, оно всегда будет соответствовать любому запросу, а преобразование 1033 никогда не будет использоваться, даже если 1033 является точным запросом языка.</span><span class="sxs-lookup"><span data-stu-id="f303d-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



