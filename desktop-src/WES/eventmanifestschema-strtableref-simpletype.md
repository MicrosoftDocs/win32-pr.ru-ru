---
title: Простой тип Стртаблереф
description: Определяет строку, которая ссылается на строку сообщения, определенную в таблице строк в манифесте или в файле сообщения (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Журнал событий простого типа Стртаблереф
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534385"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="b9939-104">Простой тип Стртаблереф</span><span class="sxs-lookup"><span data-stu-id="b9939-104">strTableRef Simple Type</span></span>

<span data-ttu-id="b9939-105">Определяет строку, которая ссылается на строку сообщения, определенную в таблице строк в манифесте или в файле сообщения (. MC).</span><span class="sxs-lookup"><span data-stu-id="b9939-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="b9939-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="b9939-106">Patterns</span></span>

<span data-ttu-id="b9939-107">Простой тип **стртаблереф** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="b9939-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="b9939-108">Строка должна иметь форму $string. *stringid* или $MC.*симболид*.</span><span class="sxs-lookup"><span data-stu-id="b9939-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="b9939-109">Если строка имеет форму, $string. *stringid*, он должен ссылаться на строку в разделе [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) манифеста.</span><span class="sxs-lookup"><span data-stu-id="b9939-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="b9939-110">Если строка имеет форму, $mc.*симболид*, она должна ссылаться на символ, определенный в файле сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9939-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9939-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b9939-111">Requirements</span></span>



| <span data-ttu-id="b9939-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b9939-112">Requirement</span></span> | <span data-ttu-id="b9939-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b9939-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b9939-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9939-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b9939-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b9939-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b9939-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9939-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b9939-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9939-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





