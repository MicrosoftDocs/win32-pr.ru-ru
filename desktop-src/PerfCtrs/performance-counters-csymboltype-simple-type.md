---
description: Определяет допустимое имя символа C/C++.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Простой тип Ксимболтипе (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998514"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="61a00-103">Простой тип Ксимболтипе (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="61a00-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="61a00-104">Определяет допустимое имя символа C/C++.</span><span class="sxs-lookup"><span data-stu-id="61a00-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="61a00-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="61a00-105">Patterns</span></span>

<span data-ttu-id="61a00-106">Простой тип **ксимболтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="61a00-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="61a00-107">Имя символа может быть пустым или содержать буквы, цифры и символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="61a00-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="61a00-108">Если указано имя, имя должно начинаться с символа подчеркивания ( \_ ) или алфавитного знака.</span><span class="sxs-lookup"><span data-stu-id="61a00-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a00-109">Требования</span><span class="sxs-lookup"><span data-stu-id="61a00-109">Requirements</span></span>



| <span data-ttu-id="61a00-110">Требование</span><span class="sxs-lookup"><span data-stu-id="61a00-110">Requirement</span></span> | <span data-ttu-id="61a00-111">Значение</span><span class="sxs-lookup"><span data-stu-id="61a00-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61a00-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61a00-112">Minimum supported client</span></span><br/> | <span data-ttu-id="61a00-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61a00-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61a00-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61a00-114">Minimum supported server</span></span><br/> | <span data-ttu-id="61a00-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61a00-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




