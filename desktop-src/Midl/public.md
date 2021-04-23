---
title: public - атрибут
description: Атрибут \ Public \ включает псевдоним, объявленный с ключевым словом typedef в библиотеке типов.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- Открытый атрибут MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650329"
---
# <a name="public-attribute"></a><span data-ttu-id="25506-104">public - атрибут</span><span class="sxs-lookup"><span data-stu-id="25506-104">public attribute</span></span>

<span data-ttu-id="25506-105">**\[ Открытый \]** атрибут включает псевдоним, объявленный с ключевым словом [**typedef**](typedef.md) в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="25506-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="25506-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25506-107">*тип данных*</span><span class="sxs-lookup"><span data-stu-id="25506-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="25506-108">Тип данных, для которого идентификатор будет псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="25506-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="25506-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="25506-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="25506-110">Другое имя, по которому *тип данных* будет известен в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="25506-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25506-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25506-111">Remarks</span></span>

<span data-ttu-id="25506-112">По умолчанию псевдоним, объявленный с [**typedef**](typedef.md) и не имеющий других атрибутов, рассматривается как **\# Определение** и не включается в библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="25506-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="25506-113">Использование атрибута **\[ Public \]** гарантирует, что псевдоним станет частью библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="25506-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="25506-114">Компилятор MIDL требует явного применения атрибута **\[ Public \]** к каждому определению typedef, которое требуется сделать открытым.</span><span class="sxs-lookup"><span data-stu-id="25506-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="25506-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="25506-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="25506-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25506-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25506-117">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="25506-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="25506-118">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="25506-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="25506-119">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="25506-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="25506-120">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="25506-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="25506-121">**определение**</span><span class="sxs-lookup"><span data-stu-id="25506-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 