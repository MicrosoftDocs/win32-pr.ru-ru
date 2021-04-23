---
title: Директивы Pragma
description: Версия-кандидат не поддерживает директивы pragma, поддерживаемые компилятором C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069981"
---
# <a name="pragma-directives"></a><span data-ttu-id="c8114-103">Директивы Pragma</span><span class="sxs-lookup"><span data-stu-id="c8114-103">Pragma Directives</span></span>

<span data-ttu-id="c8114-104">Версия-кандидат не поддерживает директивы pragma, поддерживаемые компилятором C/C++.</span><span class="sxs-lookup"><span data-stu-id="c8114-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="c8114-105">Однако версия-кандидат поддерживает следующую директиву pragma для изменения кодовой страницы:</span><span class="sxs-lookup"><span data-stu-id="c8114-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="c8114-106">Эта директива pragma не поддерживается в включенном файле ресурсов (. RC).</span><span class="sxs-lookup"><span data-stu-id="c8114-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="c8114-107">Поэтому, если у вас есть родительский RC-файл и он включает RC-файлы для нескольких языков, используйте эту директиву pragma перед включением другого RC-файла вместо использования его в самом файле прилагаемого RC-файла.</span><span class="sxs-lookup"><span data-stu-id="c8114-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="c8114-108">Это продемонстрировано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c8114-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="c8114-109">Список значений для Кодепаженум см. в разделе [идентификаторы кодовых страниц](../intl/code-page-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c8114-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 