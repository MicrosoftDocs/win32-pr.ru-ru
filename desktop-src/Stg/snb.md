---
title: СНБ (Обжидл. h)
description: Блок имени строки (СНБ) — это указатель на массив указателей на строки, который заканчивается указателем NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- снб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988427"
---
# <a name="snb"></a><span data-ttu-id="325fc-104">снб</span><span class="sxs-lookup"><span data-stu-id="325fc-104">SNB</span></span>

<span data-ttu-id="325fc-105">Блок имени строки (**СНБ**) — это указатель на массив указателей на строки, который заканчивается указателем **null** .</span><span class="sxs-lookup"><span data-stu-id="325fc-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="325fc-106">Блоки имен строк используются интерфейсом [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и вызовами функций, которые открывают объекты хранилища.</span><span class="sxs-lookup"><span data-stu-id="325fc-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="325fc-107">Строки указывают на автономные объекты хранилища или потоки, которые должны быть исключены в открытых вызовах.</span><span class="sxs-lookup"><span data-stu-id="325fc-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="325fc-108">**снб**</span><span class="sxs-lookup"><span data-stu-id="325fc-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="325fc-109">\[проводное \_ маршалирование (виреснб)\]</span><span class="sxs-lookup"><span data-stu-id="325fc-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="325fc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="325fc-110">Remarks</span></span>

<span data-ttu-id="325fc-111">**СНБ** должен быть создан путем выделения непрерывного блока памяти, в котором указатели на строки следуют **пустому** указателю, за которым следуют фактические строки.</span><span class="sxs-lookup"><span data-stu-id="325fc-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="325fc-112">Маршалирование **СНБ** основывается на предположении, что переданный **СНБ** был создан таким образом.</span><span class="sxs-lookup"><span data-stu-id="325fc-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="325fc-113">Несмотря на то, что он может храниться другими способами, **СНБ** , созданный таким образом, имеет преимущество: требуется только одна операция выделения памяти и одна свободная память для всех строк.</span><span class="sxs-lookup"><span data-stu-id="325fc-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="325fc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="325fc-114">Requirements</span></span>



| <span data-ttu-id="325fc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="325fc-115">Requirement</span></span> | <span data-ttu-id="325fc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="325fc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="325fc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="325fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="325fc-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="325fc-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="325fc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="325fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="325fc-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="325fc-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="325fc-121">Header</span><span class="sxs-lookup"><span data-stu-id="325fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="325fc-122"><dt>Обжидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="325fc-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="325fc-123">IDL</span><span class="sxs-lookup"><span data-stu-id="325fc-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="325fc-124"><dt>Обжидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="325fc-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="325fc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="325fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325fc-126">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="325fc-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





