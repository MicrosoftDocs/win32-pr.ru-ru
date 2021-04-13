---
title: Дескриптор заголовка процедуры
description: Заголовок был расширен несколько раз в течение жизненного цикла модуля NDR. Текущий компилятор по-прежнему создает разные заголовки в зависимости от режима компилятора. Однако более новые заголовки являются надмножеством более старых.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488113"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="b0d2b-105">Дескриптор заголовка процедуры</span><span class="sxs-lookup"><span data-stu-id="b0d2b-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="b0d2b-106">Заголовок был расширен несколько раз в течение жизненного цикла модуля NDR.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="b0d2b-107">Текущий компилятор по-прежнему создает разные заголовки в зависимости от режима компилятора.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="b0d2b-108">Однако более новые заголовки являются надмножеством более старых.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="b0d2b-109">Старый заголовок – OI</span><span class="sxs-lookup"><span data-stu-id="b0d2b-109">The Old –Oi Header</span></span>

<span data-ttu-id="b0d2b-110">Заголовок имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b0d2b-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="b0d2b-111">Тип обработчика \_<1> может быть одним из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="b0d2b-112">Hex</span><span class="sxs-lookup"><span data-stu-id="b0d2b-112">Hex</span></span> | <span data-ttu-id="b0d2b-113">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0d2b-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="b0d2b-114">31</span><span class="sxs-lookup"><span data-stu-id="b0d2b-114">31</span></span>  | <span data-ttu-id="b0d2b-115">FC \_ BIND \_ Generic</span><span class="sxs-lookup"><span data-stu-id="b0d2b-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="b0d2b-116">32</span><span class="sxs-lookup"><span data-stu-id="b0d2b-116">32</span></span>  | <span data-ttu-id="b0d2b-117">\_примитив привязки \_ FC</span><span class="sxs-lookup"><span data-stu-id="b0d2b-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="b0d2b-118">33</span><span class="sxs-lookup"><span data-stu-id="b0d2b-118">33</span></span>  | <span data-ttu-id="b0d2b-119">\_Автоматическая \_ Работа с FC</span><span class="sxs-lookup"><span data-stu-id="b0d2b-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="b0d2b-120">34</span><span class="sxs-lookup"><span data-stu-id="b0d2b-120">34</span></span>  | <span data-ttu-id="b0d2b-121">\_обработчик обратного вызова FC \_</span><span class="sxs-lookup"><span data-stu-id="b0d2b-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="b0d2b-122">0</span><span class="sxs-lookup"><span data-stu-id="b0d2b-122">0</span></span>   | <span data-ttu-id="b0d2b-123">(явный маркер)</span><span class="sxs-lookup"><span data-stu-id="b0d2b-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="b0d2b-124">Если тип маркера \_<1> поле имеет ненулевое значение, то процедура использует неявный маркер указанного типа.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="b0d2b-125">Дополнительные сведения см. в разделе [Handles](handles.md) .</span><span class="sxs-lookup"><span data-stu-id="b0d2b-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="b0d2b-126">Если тип маркера \_<1> поле равно нулю, то обработчик, используемый для привязки, является одним из параметров процедуры.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="b0d2b-127">Явные дескрипторы могут быть простыми, универсальными и контекстными. Последняя имеет следующий токен FC.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="b0d2b-128">Hex</span><span class="sxs-lookup"><span data-stu-id="b0d2b-128">Hex</span></span> | <span data-ttu-id="b0d2b-129">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0d2b-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="b0d2b-130">30</span><span class="sxs-lookup"><span data-stu-id="b0d2b-130">30</span></span>  | <span data-ttu-id="b0d2b-131">\_контекст привязки \_ FC</span><span class="sxs-lookup"><span data-stu-id="b0d2b-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="b0d2b-132">По соглашению типом маркера для интерфейсов DCOM является \_ Автоматическое \_ обработа FC.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="b0d2b-133">\_Флаги Oi<1> поле — это 8-разрядная маска следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="b0d2b-134">Hex</span><span class="sxs-lookup"><span data-stu-id="b0d2b-134">Hex</span></span> | <span data-ttu-id="b0d2b-135">Flag</span><span class="sxs-lookup"><span data-stu-id="b0d2b-135">Flag</span></span>                         | <span data-ttu-id="b0d2b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d2b-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="b0d2b-137">01</span><span class="sxs-lookup"><span data-stu-id="b0d2b-137">01</span></span>  | <span data-ttu-id="b0d2b-138">\_Использовано полное \_ ptr- \_ Использование OI</span><span class="sxs-lookup"><span data-stu-id="b0d2b-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="b0d2b-139">Использует полный пакет указателя.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="b0d2b-140">02</span><span class="sxs-lookup"><span data-stu-id="b0d2b-140">02</span></span>  | <span data-ttu-id="b0d2b-141">\_ \_ Использовано выделения "Oi RPCSS" \_</span><span class="sxs-lookup"><span data-stu-id="b0d2b-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="b0d2b-142">Использует пакет памяти RPCSS.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="b0d2b-143">04</span><span class="sxs-lookup"><span data-stu-id="b0d2b-143">04</span></span>  | <span data-ttu-id="b0d2b-144">\_Процедура объекта \_ OI</span><span class="sxs-lookup"><span data-stu-id="b0d2b-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="b0d2b-145">Процедура в интерфейсе объекта.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="b0d2b-146">08</span><span class="sxs-lookup"><span data-stu-id="b0d2b-146">08</span></span>  | <span data-ttu-id="b0d2b-147">Oi \_ имеет \_ рпкфлагс</span><span class="sxs-lookup"><span data-stu-id="b0d2b-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="b0d2b-148">Процедура имеет ненулевые флаги RPC.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="b0d2b-149">10</span><span class="sxs-lookup"><span data-stu-id="b0d2b-149">10</span></span>  | <span data-ttu-id="b0d2b-150">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="b0d2b-150">Oi\_\*</span></span>                       | <span data-ttu-id="b0d2b-151">Перегружен.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-151">Overloaded.</span></span>                              |
| <span data-ttu-id="b0d2b-152">20</span><span class="sxs-lookup"><span data-stu-id="b0d2b-152">20</span></span>  | <span data-ttu-id="b0d2b-153">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="b0d2b-153">Oi\_\*</span></span>                       | <span data-ttu-id="b0d2b-154">Перегружен.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-154">Overloaded.</span></span>                              |
| <span data-ttu-id="b0d2b-155">40</span><span class="sxs-lookup"><span data-stu-id="b0d2b-155">40</span></span>  | <span data-ttu-id="b0d2b-156">Oi \_ используют \_ новые \_ \_ подпрограммы init</span><span class="sxs-lookup"><span data-stu-id="b0d2b-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="b0d2b-157">Использует подпрограммы Windows NT 3.5 бета и init.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="b0d2b-158">80</span><span class="sxs-lookup"><span data-stu-id="b0d2b-158">80</span></span>  |                              | <span data-ttu-id="b0d2b-159">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-159">Unused.</span></span>                                  |



 

<span data-ttu-id="b0d2b-160">Следующие флаги перегружены.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="b0d2b-161">Hex</span><span class="sxs-lookup"><span data-stu-id="b0d2b-161">Hex</span></span> | <span data-ttu-id="b0d2b-162">Flag</span><span class="sxs-lookup"><span data-stu-id="b0d2b-162">Flag</span></span>                                    | <span data-ttu-id="b0d2b-163">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d2b-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="b0d2b-164">10</span><span class="sxs-lookup"><span data-stu-id="b0d2b-164">10</span></span>  | <span data-ttu-id="b0d2b-165">используется КОДИРОВКа \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0d2b-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="b0d2b-166">Используется только в поле выбора.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="b0d2b-167">20</span><span class="sxs-lookup"><span data-stu-id="b0d2b-167">20</span></span>  | <span data-ttu-id="b0d2b-168">используется декодирование \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0d2b-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="b0d2b-169">Используется только в поле выбора.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="b0d2b-170">10</span><span class="sxs-lookup"><span data-stu-id="b0d2b-170">10</span></span>  | <span data-ttu-id="b0d2b-171">\_Обработка исключений Oi игнорирования \_ объектов \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0d2b-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="b0d2b-172">Больше не используется (старый OLE).</span><span class="sxs-lookup"><span data-stu-id="b0d2b-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="b0d2b-173">20</span><span class="sxs-lookup"><span data-stu-id="b0d2b-173">20</span></span>  | <span data-ttu-id="b0d2b-174">В Oi \_ есть \_ канал \_ или \_ сбой</span><span class="sxs-lookup"><span data-stu-id="b0d2b-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="b0d2b-175">Только в необработанных RPC, \[ канале связи \_ , \_ состоянии сбоя \] .</span><span class="sxs-lookup"><span data-stu-id="b0d2b-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="b0d2b-176">20</span><span class="sxs-lookup"><span data-stu-id="b0d2b-176">20</span></span>  | <span data-ttu-id="b0d2b-177">В файле Oi \_ obj \_ используется \_ \_ интерпретатор v2</span><span class="sxs-lookup"><span data-stu-id="b0d2b-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="b0d2b-178">Только в DCOM используйте интерпретатор [**– ОИФ**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="b0d2b-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="b0d2b-179">В \_ поле "флаги rpc<4>" описывается, как задать поле **рпкфлагс** структуры [**\_ сообщения RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) .</span><span class="sxs-lookup"><span data-stu-id="b0d2b-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="b0d2b-180">Это поле имеется только в том случае, если для \_ флагов oi<1 \_> \_ задано значение Oi рпкфлагс.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="b0d2b-181">Если это поле отсутствует, то флаги RPC для удаленной процедуры будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="b0d2b-182">Для повышения производительности в асинхронных интерпретаторах всегда отображается \_ поле Флаги rpc<4>.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="b0d2b-183">В \_ поле proc num<2> содержится номер процедуры процедуры.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="b0d2b-184">Размер стека \_<2> предоставляет общий размер всех параметров в стеке, включая все этот указатель и (или) возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="b0d2b-185">Явное \_ Описание обработчика \_<> поле описано далее в этом документе.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="b0d2b-186">Это поле отсутствует, если процедура использует неявный обработчик.</span><span class="sxs-lookup"><span data-stu-id="b0d2b-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 