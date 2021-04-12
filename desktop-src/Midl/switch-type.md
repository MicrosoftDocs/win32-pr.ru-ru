---
title: switch_type - атрибут
description: Атрибут \ Switch \_ Type \ определяет тип переменной, используемой в качестве discriminant объединения. Тип переключателя может быть целым числом, символом, логическим значением или типом перечисления.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type атрибута MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889691"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="ec1ca-105">\_атрибут типа Switch</span><span class="sxs-lookup"><span data-stu-id="ec1ca-105">switch\_type attribute</span></span>

<span data-ttu-id="ec1ca-106">Атрибут **\[ \_ типа \] switch** определяет тип переменной, используемой в качестве discriminant объединения.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="ec1ca-107">Тип переключателя может быть целым числом, символом, логическим значением или типом перечисления.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="ec1ca-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec1ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1ca-109">*спецификатор типа-Switch*</span><span class="sxs-lookup"><span data-stu-id="ec1ca-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ec1ca-110">Задает тип [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)или [**enum**](enum.md) или идентификатор такого типа.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec1ca-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec1ca-111">Remarks</span></span>

<span data-ttu-id="ec1ca-112">В то время как атрибут **\[ \_ типа \] switch** определяет тип переменной, параметр **\[** [**\_ —**](switch-is.md) **\]** Attribute указывает имя параметра, который является discriminant объединения.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="ec1ca-113">Атрибут **\[ \_ типа \] switch** применяется к параметрам или элементам структур или объединений.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="ec1ca-114">Объединение и его discriminant должны быть указаны на том же логическом уровне.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="ec1ca-115">Если Union является параметром, discriminant объединения должен быть другим параметром.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="ec1ca-116">Если объединение является полем структуры, discriminant должно быть другим полем структуры на том же уровне, что и поле Union.</span><span class="sxs-lookup"><span data-stu-id="ec1ca-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="ec1ca-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec1ca-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="ec1ca-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec1ca-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1ca-119">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-120">**char**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-121">Инкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="ec1ca-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-122">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-123">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="ec1ca-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-124">**INT**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-125">Неинкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="ec1ca-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-126">**параметр \_ имеет**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="ec1ca-127">**наборов**</span><span class="sxs-lookup"><span data-stu-id="ec1ca-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




