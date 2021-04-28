---
description: Простой тип Ксимболтипе (счетчики производительности) — определяет допустимое имя символа C/C++.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Простой тип Ксимболтипе (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084232"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="88d1e-103">Простой тип Ксимболтипе (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="88d1e-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="88d1e-104">Определяет допустимое имя символа C/C++.</span><span class="sxs-lookup"><span data-stu-id="88d1e-104">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="88d1e-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="88d1e-105">Patterns</span></span>

<span data-ttu-id="88d1e-106">Простой тип **ксимболтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="88d1e-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="88d1e-107">Имя символа может быть пустым или содержать буквы, цифры и символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="88d1e-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="88d1e-108">Если указано имя, имя должно начинаться с символа подчеркивания ( \_ ) или алфавитного знака.</span><span class="sxs-lookup"><span data-stu-id="88d1e-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d1e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="88d1e-109">Requirements</span></span>



| <span data-ttu-id="88d1e-110">Требование</span><span class="sxs-lookup"><span data-stu-id="88d1e-110">Requirement</span></span> | <span data-ttu-id="88d1e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="88d1e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88d1e-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88d1e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="88d1e-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88d1e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88d1e-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88d1e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="88d1e-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88d1e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




