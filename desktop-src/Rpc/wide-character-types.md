---
title: Типы Wide-Character
description: Microsoft RPC поддерживает широкий тип символов WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134263"
---
# <a name="wide-character-types"></a><span data-ttu-id="c09ab-103">Типы Wide-Character</span><span class="sxs-lookup"><span data-stu-id="c09ab-103">Wide-Character Types</span></span>

<span data-ttu-id="c09ab-104">Microsoft RPC поддерживает широкий тип символов [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t).</span><span class="sxs-lookup"><span data-stu-id="c09ab-104">Microsoft RPC supports the wide-character type [**wchar\_t**](/windows/desktop/Midl/wchar-t).</span></span> <span data-ttu-id="c09ab-105">Тип расширенных символов использует 2 байта для каждого символа.</span><span class="sxs-lookup"><span data-stu-id="c09ab-105">The wide-character type uses 2 bytes for each character.</span></span> <span data-ttu-id="c09ab-106">Определение языка ANSI C позволяет инициализировать длинные и длинные строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c09ab-106">The ANSI C-language definition allows you to initialize long characters and long strings as:</span></span>

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 