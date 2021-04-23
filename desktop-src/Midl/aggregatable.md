---
title: aggregatable - атрибут
description: Атрибут \ агрегированный \ указывает, что класс поддерживает агрегирование.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- статистически обрабатываемый атрибут MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337084"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="e3558-104">aggregatable - атрибут</span><span class="sxs-lookup"><span data-stu-id="e3558-104">aggregatable attribute</span></span>

<span data-ttu-id="e3558-105">**\[ Статистический \]** атрибут указывает, что класс поддерживает агрегирование.</span><span class="sxs-lookup"><span data-stu-id="e3558-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="e3558-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3558-107">*Список атрибутов coclass*</span><span class="sxs-lookup"><span data-stu-id="e3558-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3558-108">Другие атрибуты, которые применяются к классу.</span><span class="sxs-lookup"><span data-stu-id="e3558-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="e3558-109">*имя класса*</span><span class="sxs-lookup"><span data-stu-id="e3558-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3558-110">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="e3558-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="e3558-111">*coclass-интерфейс-список*</span><span class="sxs-lookup"><span data-stu-id="e3558-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3558-112">Список интерфейсов для класса.</span><span class="sxs-lookup"><span data-stu-id="e3558-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3558-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3558-113">Remarks</span></span>

<span data-ttu-id="e3558-114">Используйте **\[ \] статистический** атрибут в операторе [**coclass**](coclass.md) , чтобы пользователи могли понять, что класс поддерживает агрегирование.</span><span class="sxs-lookup"><span data-stu-id="e3558-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="e3558-115">То есть класс позволяет предоставлять его интерфейсы классом контейнера, как если бы эти интерфейсы были собственными интерфейсами контейнера.</span><span class="sxs-lookup"><span data-stu-id="e3558-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="e3558-116">Представление типефлаг для этого атрибута — ТИПЕФЛАГ \_ фаггрегатабле.</span><span class="sxs-lookup"><span data-stu-id="e3558-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="e3558-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="e3558-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="e3558-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3558-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3558-119">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="e3558-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="e3558-120">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="e3558-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e3558-121">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="e3558-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e3558-122">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="e3558-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 