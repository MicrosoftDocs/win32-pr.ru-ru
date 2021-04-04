---
title: переключить атрибут
description: Ключевое слово Switch выбирает discriminant для инкапсулированного \_ объединения.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- параметр атрибута MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986981"
---
# <a name="switch-attribute"></a><span data-ttu-id="0d08a-104">переключить атрибут</span><span class="sxs-lookup"><span data-stu-id="0d08a-104">switch attribute</span></span>

<span data-ttu-id="0d08a-105">Ключевое слово **switch** выбирает discriminant для [**инкапсулированного \_ объединения**](encapsulated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="0d08a-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="0d08a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d08a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d08a-107">*Тип переключателя*</span><span class="sxs-lookup"><span data-stu-id="0d08a-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0d08a-108">Задает тип [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) или идентификатор, который разрешается в один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="0d08a-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="0d08a-109">*имя коммутатора*</span><span class="sxs-lookup"><span data-stu-id="0d08a-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0d08a-110">Задает имя переменной *типа Switch-Type* , которая выступает в качестве discriminant объединения.</span><span class="sxs-lookup"><span data-stu-id="0d08a-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0d08a-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d08a-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="0d08a-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d08a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d08a-113">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="0d08a-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0d08a-114">Неинкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="0d08a-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="0d08a-115">**параметр \_ имеет**</span><span class="sxs-lookup"><span data-stu-id="0d08a-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="0d08a-116">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="0d08a-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="0d08a-117">**наборов**</span><span class="sxs-lookup"><span data-stu-id="0d08a-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




