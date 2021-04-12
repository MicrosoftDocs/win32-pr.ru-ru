---
description: Определяет тип, содержащий допустимые значения для атрибута Type элемента Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Простой тип Маргинтипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272308"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="332f9-103">Простой тип Маргинтипетипе</span><span class="sxs-lookup"><span data-stu-id="332f9-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="332f9-104">Определяет тип, содержащий допустимые значения для атрибута **Type** [элемента Margin](margin-element.md).</span><span class="sxs-lookup"><span data-stu-id="332f9-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="332f9-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="332f9-105">Patterns</span></span>

<span data-ttu-id="332f9-106">Простой тип **маргинтипетипе** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="332f9-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="332f9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="332f9-107">Remarks</span></span>

<span data-ttu-id="332f9-108">Допустимые значения для атрибута **Type** [элемента Margin](margin-element.md) : Left и right.</span><span class="sxs-lookup"><span data-stu-id="332f9-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="332f9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="332f9-109">Requirements</span></span>



| <span data-ttu-id="332f9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="332f9-110">Requirement</span></span> | <span data-ttu-id="332f9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="332f9-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="332f9-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="332f9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="332f9-113">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="332f9-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="332f9-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="332f9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="332f9-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="332f9-115">None supported</span></span><br/>                                     |



 

 




