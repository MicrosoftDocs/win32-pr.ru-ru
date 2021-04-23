---
title: Сериализация процедур
description: При использовании сериализации процедуры процедура помечается атрибутом \ Encoded \ или \ дешифровки \. Вместо создания обычной удаленной заглушки компилятор создает заглушку сериализации для подпрограммы.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424145"
---
# <a name="procedure-serialization"></a><span data-ttu-id="c1fc9-104">Сериализация процедур</span><span class="sxs-lookup"><span data-stu-id="c1fc9-104">Procedure Serialization</span></span>

<span data-ttu-id="c1fc9-105">При использовании сериализации процедуры процедура помечается \[ [](/windows/desktop/Midl/encode) \] атрибутом кодирования или \[ [**декодирования**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="c1fc9-105">When you use procedure serialization, a procedure is labeled with the \[[**encode**](/windows/desktop/Midl/encode)\] or \[[**decode**](/windows/desktop/Midl/decode)\] attribute.</span></span> <span data-ttu-id="c1fc9-106">Вместо создания обычной удаленной заглушки компилятор создает заглушку сериализации для подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-106">Instead of generating the usual remote stub, the compiler generates a serialization stub for the routine.</span></span>

<span data-ttu-id="c1fc9-107">Так же, как Удаленная процедура должна использовать для удаленного вызова маркер привязки, процедура сериализации должна использовать для работы со службами сериализации обработчик сериализации.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-107">Just as a remote procedure must use a binding handle to make a remote call, a serialization procedure must use a serialization handle to use serialization services.</span></span> <span data-ttu-id="c1fc9-108">Если не указан маркер сериализации, для направления вызова используется неявный обработчик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-108">If a serialization handle is not specified, a default implicit handle is used to direct the call.</span></span> <span data-ttu-id="c1fc9-109">С другой стороны, если указан маркер сериализации либо как явный аргумент [**Handle \_**](/windows/desktop/Midl/handle-t) в подпрограммы, либо с помощью \[ [**явного атрибута \_ Handle**](/windows/desktop/Midl/explicit-handle) \] , необходимо передать допустимый обработчик в качестве аргумента вызова.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-109">On the other hand, if the serialization handle is specified, either as an explicit [**handle\_t**](/windows/desktop/Midl/handle-t) argument of the routine or by using the \[[**explicit\_handle**](/windows/desktop/Midl/explicit-handle)\] attribute, you must pass a valid handle as an argument of the call.</span></span> <span data-ttu-id="c1fc9-110">Дополнительные сведения о создании допустимого дескриптора сериализации см. в статьях [дескрипторы сериализации](serialization-handles.md), [примеры фиксированной кодировки буфера](fixed-buffer-serialization.md)и [примеры добавочной кодировки](examples-of-incremental-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="c1fc9-110">For additional information on how to create a valid serialization handle, see [Serialization Handles](serialization-handles.md), [Examples of Fixed Buffer Encoding](fixed-buffer-serialization.md), and [Examples of Incremental Encoding](examples-of-incremental-encoding.md).</span></span>

> [!Note]
> <span data-ttu-id="c1fc9-111">Microsoft RPC позволяет смешивать процедуры удаленной и сериализации в одном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-111">Microsoft RPC allows remote and serialization procedures to be mixed in one interface.</span></span> <span data-ttu-id="c1fc9-112">Однако при этом следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-112">However, use caution when doing so.</span></span>
> 
> <span data-ttu-id="c1fc9-113">Для удаленных процедур с неявными дескрипторами привязки компилятор MIDL создает переменную глобального дескриптора типа [**Handle \_ t**](/windows/desktop/Midl/handle-t).</span><span class="sxs-lookup"><span data-stu-id="c1fc9-113">For remote procedures with implicit binding handles, the MIDL compiler generates a global handle variable of type [**handle\_t**](/windows/desktop/Midl/handle-t).</span></span> <span data-ttu-id="c1fc9-114">Процедуры и типы с неявными дескрипторами сериализации используют эту же глобальную переменную дескриптора.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-114">Procedures and types with implicit serialization handles use this same global handle variable.</span></span>
> 
> <span data-ttu-id="c1fc9-115">Для неявных дескрипторов в глобальном неявном дескрипторе должен быть задан допустимый дескриптор привязки перед удаленным вызовом.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-115">For implicit handles, the global implicit handle must be set to a valid binding handle before a remote call.</span></span> <span data-ttu-id="c1fc9-116">Перед вызовом сериализации неявный обработчик должен быть установлен в допустимый обработчик сериализации.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-116">The implicit handle must be set to a valid serialization handle before a serialization call.</span></span> <span data-ttu-id="c1fc9-117">Поэтому процедура не может быть одновременно удаленной и сериализованной.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-117">Therefore, a procedure cannot be both remote and serialized.</span></span> <span data-ttu-id="c1fc9-118">Он должен быть одним или другим.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-118">It must be one or the other.</span></span>

 

 

 