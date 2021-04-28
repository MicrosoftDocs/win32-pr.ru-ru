---
title: Простой тип Ксимболтипе (журнал событий Windows)
description: Простой тип Ксимболтипе (журнал событий Windows) — определяет допустимое имя символа C/C++.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Журнал событий простого типа Ксимболтипе
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090622"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="fccf9-104">Простой тип Ксимболтипе (журнал событий Windows)</span><span class="sxs-lookup"><span data-stu-id="fccf9-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="fccf9-105">Определяет допустимое имя символа C/C++.</span><span class="sxs-lookup"><span data-stu-id="fccf9-105">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="fccf9-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="fccf9-106">Patterns</span></span>

<span data-ttu-id="fccf9-107">Простой тип **ксимболтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="fccf9-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="fccf9-108">Имя символа может быть пустым или содержать буквы, цифры и символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="fccf9-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="fccf9-109">Если имя пустое, компилятор сообщений создаст имя символа.</span><span class="sxs-lookup"><span data-stu-id="fccf9-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="fccf9-110">Если указано имя, имя должно начинаться с символа подчеркивания ( \_ ) или алфавитного знака.</span><span class="sxs-lookup"><span data-stu-id="fccf9-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="fccf9-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="fccf9-111">Remarks</span></span>

<span data-ttu-id="fccf9-112">Если имя символа пустое, компилятор сообщений использует атрибут **Name** элемента, который вы определяете для создания имени символа.</span><span class="sxs-lookup"><span data-stu-id="fccf9-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="fccf9-113">Компилятор заменяет любые символы, отличные от алфавитно-цифровых, и начальные цифры символами подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="fccf9-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="fccf9-114">Например, если атрибуту **имени** канала является Microsoft-Windows-Самплепровидер/эксплуатация, компилятор будет использовать Microsoft \_ Windows самплепровидер в \_ \_ качестве имени символа.</span><span class="sxs-lookup"><span data-stu-id="fccf9-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fccf9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fccf9-115">Requirements</span></span>



| <span data-ttu-id="fccf9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fccf9-116">Requirement</span></span> | <span data-ttu-id="fccf9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fccf9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fccf9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fccf9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fccf9-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fccf9-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fccf9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fccf9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fccf9-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fccf9-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





