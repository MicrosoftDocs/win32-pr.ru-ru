---
description: Класс Локкит является внутренним классом, который блокирует и разблокирует DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Класс Имедиаобжектимпл:: Локкит (Дмоимпл. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675178"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="891c3-103">Класс Имедиаобжектимпл:: Локкит</span><span class="sxs-lookup"><span data-stu-id="891c3-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="891c3-104">`LockIt`Класс является внутренним классом, который блокирует и разблокирует DMO.</span><span class="sxs-lookup"><span data-stu-id="891c3-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="891c3-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="891c3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891c3-106"><span id="p"></span><span id="P"></span>*ш*</span><span class="sxs-lookup"><span data-stu-id="891c3-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="891c3-107">Указатель на производный объект.</span><span class="sxs-lookup"><span data-stu-id="891c3-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="891c3-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="891c3-108">Remarks</span></span>

<span data-ttu-id="891c3-109">`LockIt`Конструктор БЛОКИРУЕТ DMO, а деструктор разблокирует DMO.</span><span class="sxs-lookup"><span data-stu-id="891c3-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="891c3-110">Чтобы заблокировать объект внутри производного класса, Объявите локальную переменную типа `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="891c3-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="891c3-111">Объекты DMO блокируются, пока `LockIt` объект остается в области:</span><span class="sxs-lookup"><span data-stu-id="891c3-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="891c3-112">Методы в **имедиаобжектимпл** автоматически блокируют DMO.</span><span class="sxs-lookup"><span data-stu-id="891c3-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="891c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="891c3-113">Requirements</span></span>



| <span data-ttu-id="891c3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="891c3-114">Requirement</span></span> | <span data-ttu-id="891c3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="891c3-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891c3-116">Header</span><span class="sxs-lookup"><span data-stu-id="891c3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="891c3-117"><dt>Дмоимпл. h</dt></span><span class="sxs-lookup"><span data-stu-id="891c3-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="891c3-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="891c3-118">Library</span></span><br/> | <dl> <span data-ttu-id="891c3-119"><dt>Дмогуидс. lib; </dt> <dt>Мсдмо. lib</dt></span><span class="sxs-lookup"><span data-stu-id="891c3-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="891c3-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="891c3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891c3-121">**Шаблон класса Имедиаобжектимпл**</span><span class="sxs-lookup"><span data-stu-id="891c3-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




