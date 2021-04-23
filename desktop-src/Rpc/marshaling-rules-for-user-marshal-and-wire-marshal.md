---
title: Правила маршалирования для user_marshal и wire_marshal
description: В спецификации использование-DCE для маршалирования внедренных типов указателей необходимо учитывать следующие ограничения при реализации \_ функций Type усерсизе, Type \_ усермаршал и \_ усерунмаршал Type.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792793"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="52d05-103">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="52d05-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="52d05-104">В спецификации использование-DCE для маршалирования внедренных типов указателей необходимо учитывать следующие ограничения при реализации <type> \_ функций усерсизе, <type> \_ усермаршал и <type> \_ усерунмаршал.</span><span class="sxs-lookup"><span data-stu-id="52d05-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="52d05-105">(Правила и примеры, приведенные здесь, предназначены для маршалирования.</span><span class="sxs-lookup"><span data-stu-id="52d05-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="52d05-106">Однако подпрограммы изменения размера и распаковки должны соответствовать тем же ограничениям:</span><span class="sxs-lookup"><span data-stu-id="52d05-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="52d05-107">Если тип связи является плоским типом без указателей, подпрограммы упаковки для соответствующего усерм-типа должны просто маршалировать данные в соответствии с макетом типа связи.</span><span class="sxs-lookup"><span data-stu-id="52d05-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="52d05-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="52d05-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="52d05-109">Обратите внимание, что тип провода, **Long**, является плоским типом.</span><span class="sxs-lookup"><span data-stu-id="52d05-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="52d05-110">ОБРАБОТЧИК обрабатывает \_ \_ функцию усермаршал в **течение длительного времени** при \_ передаче ему объекта обработчика обработчика.</span><span class="sxs-lookup"><span data-stu-id="52d05-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="52d05-111">Если тип связи является указателем на другой тип, подпрограммы упаковки для соответствующего усерм-типа должны маршалировать данные в соответствии с макетом для типа, на который указывает тип связи.</span><span class="sxs-lookup"><span data-stu-id="52d05-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="52d05-112">Подсистема доставки ОНД отвечает за указатель.</span><span class="sxs-lookup"><span data-stu-id="52d05-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="52d05-113">Пример:</span><span class="sxs-lookup"><span data-stu-id="52d05-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="52d05-114">Обратите внимание, что тип провода, **\_ Тип провода**, является типом указателя.</span><span class="sxs-lookup"><span data-stu-id="52d05-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="52d05-115">\_ \_ Функция УСЕРМАРШАЛ данных Handle маршалирует данные, связанные с этим маркером, используя макет хдата, а не \* Макет хдата.</span><span class="sxs-lookup"><span data-stu-id="52d05-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="52d05-116">Тип связи должен быть либо плоским типом данных, либо типом указателя.</span><span class="sxs-lookup"><span data-stu-id="52d05-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="52d05-117">Если тип трансмиссибле должен быть чем-то другим (например, структурой с указателями), используйте указатель на нужный тип в качестве типа связи.</span><span class="sxs-lookup"><span data-stu-id="52d05-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="52d05-118">Применение этих ограничений заключается в том, что типы, определенные \[ атрибутами " [**проводное \_ маршалирование**](/windows/desktop/Midl/wire-marshal) " \] или " \[ [**пользовательское \_ маршалирование**](/windows/desktop/Midl/user-marshal) ", \] можно свободно внедрять в другие типы.</span><span class="sxs-lookup"><span data-stu-id="52d05-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52d05-119">См. также</span><span class="sxs-lookup"><span data-stu-id="52d05-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52d05-120">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="52d05-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="52d05-121">**Пользовательская \_ Упаковка**</span><span class="sxs-lookup"><span data-stu-id="52d05-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="52d05-122">Тип \_ Усерсизе функция</span><span class="sxs-lookup"><span data-stu-id="52d05-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="52d05-123">Тип \_ Усермаршал функция</span><span class="sxs-lookup"><span data-stu-id="52d05-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="52d05-124">Сетипе \_ усерунмаршалфунктион</span><span class="sxs-lookup"><span data-stu-id="52d05-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="52d05-125">Сетипе \_ усерфрифунктион</span><span class="sxs-lookup"><span data-stu-id="52d05-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 