---
title: pointer_default - атрибут
description: Атрибут \ указатель \_ по умолчанию \ задает атрибут указателя по умолчанию для всех указателей, за исключением указателей верхнего уровня, которые отображаются в списках параметров.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default атрибута MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069858"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="19014-104">\_атрибут указателя по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19014-104">pointer\_default attribute</span></span>

<span data-ttu-id="19014-105">Атрибут **\[ указателя \_ по \] умолчанию** задает атрибут указателя по умолчанию для всех указателей, за исключением указателей верхнего уровня, которые отображаются в списках параметров.</span><span class="sxs-lookup"><span data-stu-id="19014-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="19014-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19014-106">Parameters</span></span>

<span data-ttu-id="19014-107">Этот атрибут не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="19014-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="19014-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="19014-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="19014-109">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19014-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19014-110">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="19014-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="19014-111">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="19014-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="19014-112">**массивы**</span><span class="sxs-lookup"><span data-stu-id="19014-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="19014-113">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="19014-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="19014-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="19014-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="19014-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="19014-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="19014-116">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="19014-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="19014-117">Типы указателей по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19014-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 