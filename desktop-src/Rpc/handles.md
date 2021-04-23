---
title: Маркеры
description: Столько же, сколько в строке формата в описании дескрипторов адресов процедур.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338716"
---
# <a name="handles"></a><span data-ttu-id="98809-103">Маркеры</span><span class="sxs-lookup"><span data-stu-id="98809-103">Handles</span></span>

<span data-ttu-id="98809-104">Столько же, сколько в строке формата в описании дескрипторов адресов процедур.</span><span class="sxs-lookup"><span data-stu-id="98809-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="98809-105">Первая часть — это тип дескриптора \_<1> поле описания процедуры, используемое для указания неявных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="98809-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="98809-106">Эта часть всегда имеется.</span><span class="sxs-lookup"><span data-stu-id="98809-106">This part is always present.</span></span> <span data-ttu-id="98809-107">Вторая часть представляет собой описание параметра любого явного маркера в процедуре.</span><span class="sxs-lookup"><span data-stu-id="98809-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="98809-108">Оба описания описаны в следующих разделах, а также описание дополнительной поддержки компилятора MIDL для структуры дескриптора-заглушки для проблем с дескрипторами привязки.</span><span class="sxs-lookup"><span data-stu-id="98809-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="98809-109">Неявные дескрипторы</span><span class="sxs-lookup"><span data-stu-id="98809-109">Implicit Handles</span></span>

<span data-ttu-id="98809-110">Если процедура использует неявный обработчик для привязки, тип обработки \_<1> поле описания процедуры содержит одно из трех допустимых ненулевых значений.</span><span class="sxs-lookup"><span data-stu-id="98809-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="98809-111">Поддержка компилятора MIDL для неявных дескрипторов находится в поле неявных \_ сведений дескриптора в \_ структуре дескриптора-заглушки:</span><span class="sxs-lookup"><span data-stu-id="98809-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="98809-112">Если процедура использует автоматическую обработку, элемент **паутохандле** содержит адрес заданной заглушки — Auto Handles Variable.</span><span class="sxs-lookup"><span data-stu-id="98809-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="98809-113">Если в процедуре используется неявный примитивный маркер, элемент **ппримитивехандле** содержит адрес переменной-заглушки, заданной в качестве маркера.</span><span class="sxs-lookup"><span data-stu-id="98809-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="98809-114">Наконец, если в процедуре используется неявный универсальный маркер, элемент **пженерикбиндингинфо** содержит адрес указателя на соответствующую структуру **\_ \_ сведений об универсальной привязке** .</span><span class="sxs-lookup"><span data-stu-id="98809-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="98809-115">Параметр- **\_ заглушка \_** структуры данных MIDL содержит указатель на коллекцию структурных **\_ \_ пар универсальных привязок** .</span><span class="sxs-lookup"><span data-stu-id="98809-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="98809-116">Запись в нулевой положении этой коллекции зарезервирована для подпрограмм **привязки** и отмены **привязки** , соответствующих универсальному маркеру привязки, на который ссылается **пженерикбиндингинфо** в **неявных \_ \_ сведениях о обработчике**.</span><span class="sxs-lookup"><span data-stu-id="98809-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="98809-117">Тип неявного маркера привязки указан в строке формата.</span><span class="sxs-lookup"><span data-stu-id="98809-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="98809-118">Явные дескрипторы</span><span class="sxs-lookup"><span data-stu-id="98809-118">Explicit Handles</span></span>

<span data-ttu-id="98809-119">Существует три возможных типа явных обработчиков: Context, Generic и примитив.</span><span class="sxs-lookup"><span data-stu-id="98809-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="98809-120">В случае явного маркера (или \[ **выходного** \] обработчика, который обрабатывается таким же образом) сведения о обработчике привязки отображаются как один из параметров процедуры.</span><span class="sxs-lookup"><span data-stu-id="98809-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="98809-121">Ниже приведены три возможных описания.</span><span class="sxs-lookup"><span data-stu-id="98809-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="98809-122">Примитивные</span><span class="sxs-lookup"><span data-stu-id="98809-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="98809-123">Флаг<1> указывает, передается ли этот маркер указателем.</span><span class="sxs-lookup"><span data-stu-id="98809-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="98809-124">Смещение<2> предоставляет смещение от начала стека до маркера-примитива.</span><span class="sxs-lookup"><span data-stu-id="98809-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="98809-125">Описание примитивного маркера в строке формата типа сокращается до одного раздела, который не учитывается в корпусе FC \_ .</span><span class="sxs-lookup"><span data-stu-id="98809-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="98809-126">Универсальный шаблон</span><span class="sxs-lookup"><span data-stu-id="98809-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="98809-127">Флаг \_ и \_ Размер<1> имеют верхний флаг и нижний размер.</span><span class="sxs-lookup"><span data-stu-id="98809-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="98809-128">Флаг указывает, передается ли маркер указателем.</span><span class="sxs-lookup"><span data-stu-id="98809-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="98809-129">В поле Размер указывается размер определяемого пользователем типа универсального маркера.</span><span class="sxs-lookup"><span data-stu-id="98809-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="98809-130">Этот размер ограничен 1, 2 или 4 байтами на 32-разрядных системах и 1, 2, 4 или 8 байтами на 64-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="98809-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="98809-131">Поле offset<2> предоставляет смещение от начала стека указателя до данных заданного размера.</span><span class="sxs-lookup"><span data-stu-id="98809-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="98809-132">\_Индекс пары подпрограммы привязки \_ \_<1> поле предоставляет индекс в поле Аженерикбиндинграутинепаирс дескриптора заглушки для указателей функций **BIND** и **Unbind** для универсального дескриптора.</span><span class="sxs-lookup"><span data-stu-id="98809-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="98809-133">Описание универсального маркера в формате типа является описанием только связанного типа данных.</span><span class="sxs-lookup"><span data-stu-id="98809-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="98809-134">Контекст</span><span class="sxs-lookup"><span data-stu-id="98809-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="98809-135">Флаги<1> указать способ передачи маркера и его тип.</span><span class="sxs-lookup"><span data-stu-id="98809-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="98809-136">В следующей таблице показаны допустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="98809-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="98809-137">Hex</span><span class="sxs-lookup"><span data-stu-id="98809-137">Hex</span></span> | <span data-ttu-id="98809-138">Flag</span><span class="sxs-lookup"><span data-stu-id="98809-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="98809-139">80</span><span class="sxs-lookup"><span data-stu-id="98809-139">80</span></span>  | <span data-ttu-id="98809-140">параметр HANDLE обрабатывается \_ \_ \_ через \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="98809-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="98809-141">40</span><span class="sxs-lookup"><span data-stu-id="98809-141">40</span></span>  | <span data-ttu-id="98809-142">параметр ОБРАБОТЧИКа \_ \_ находится \_ в</span><span class="sxs-lookup"><span data-stu-id="98809-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="98809-143">20</span><span class="sxs-lookup"><span data-stu-id="98809-143">20</span></span>  | <span data-ttu-id="98809-144">параметр ОБРАБОТЧИКа \_ \_ \_ исходящий</span><span class="sxs-lookup"><span data-stu-id="98809-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="98809-145">21</span><span class="sxs-lookup"><span data-stu-id="98809-145">21</span></span>  | <span data-ttu-id="98809-146">\_ \_ \_ ВОЗВРАЩАЕМый параметр Handle</span><span class="sxs-lookup"><span data-stu-id="98809-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="98809-147">08</span><span class="sxs-lookup"><span data-stu-id="98809-147">08</span></span>  | <span data-ttu-id="98809-148">\_четкий \_ маркер контекста NDR \_</span><span class="sxs-lookup"><span data-stu-id="98809-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="98809-149">04</span><span class="sxs-lookup"><span data-stu-id="98809-149">04</span></span>  | <span data-ttu-id="98809-150">\_ \_ несериализуемый обработчик контекста \_ NDR \_</span><span class="sxs-lookup"><span data-stu-id="98809-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="98809-151">02</span><span class="sxs-lookup"><span data-stu-id="98809-151">02</span></span>  | <span data-ttu-id="98809-152">\_ \_ сериализация обработчика контекста ОНД \_</span><span class="sxs-lookup"><span data-stu-id="98809-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="98809-153">01</span><span class="sxs-lookup"><span data-stu-id="98809-153">01</span></span>  | <span data-ttu-id="98809-154">\_маркер контекста \_ ОНД \_ не может \_ иметь \_ значение null</span><span class="sxs-lookup"><span data-stu-id="98809-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="98809-155">Первые четыре флага всегда присутствовали, последние четыре были добавлены в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="98809-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="98809-156">Поле offset<2> предоставляет смещение от начала стека до маркера контекста.</span><span class="sxs-lookup"><span data-stu-id="98809-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="98809-157">\_ \_ Индекс подпрограммы очистки контекста \_<1> предоставляет индекс в поле **апфнндррундовнраутинес** дескриптора заглушки для подпрограммы очистки, используемой для этого дескриптора контекста.</span><span class="sxs-lookup"><span data-stu-id="98809-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="98809-158">Компилятор всегда создает индекс.</span><span class="sxs-lookup"><span data-stu-id="98809-158">The compiler always generates an index.</span></span> <span data-ttu-id="98809-159">Для подпрограмм, не имеющих подпрограммы очистки, это индекс для позиции таблицы, которая содержит значение null.</span><span class="sxs-lookup"><span data-stu-id="98809-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="98809-160">Для заглушек, встроенного в **– Oi2**, параметр \_ num<1> предоставляет порядковый номер, начинающийся с нуля, указывая, какой именно обработчик контекста находится в данной процедуре.</span><span class="sxs-lookup"><span data-stu-id="98809-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="98809-161">Для предыдущих версий интерпретатора параметр \_ num<1> предоставляет номер параметра маркера контекста, начинающийся с нуля, в процедуре.</span><span class="sxs-lookup"><span data-stu-id="98809-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="98809-162">Описание обработчика контекста в строке формата типа не будет содержать смещение<2> в описании.</span><span class="sxs-lookup"><span data-stu-id="98809-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="98809-163">Новый заголовок – ОИФ</span><span class="sxs-lookup"><span data-stu-id="98809-163">The New –Oif Header</span></span>

<span data-ttu-id="98809-164">Как упоминалось ранее, заголовок [**– ОИФ**](/windows/desktop/Midl/-oi) разворачивается в заголовке **– Oi** .</span><span class="sxs-lookup"><span data-stu-id="98809-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="98809-165">Для удобства здесь показаны все поля:</span><span class="sxs-lookup"><span data-stu-id="98809-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="98809-166">(Старый заголовок)</span><span class="sxs-lookup"><span data-stu-id="98809-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="98809-167">(Расширения [**– ОИФ**](/windows/desktop/Midl/-oi) )</span><span class="sxs-lookup"><span data-stu-id="98809-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="98809-168">Постоянный \_ \_ Размер буфера клиента \_<2> предоставляет размер буфера упаковки, который мог быть предварительно вычислен компилятором.</span><span class="sxs-lookup"><span data-stu-id="98809-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="98809-169">Это может быть только частичный размер, так как флаг Клиентмустсизе инициирует изменение размера.</span><span class="sxs-lookup"><span data-stu-id="98809-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="98809-170">\_ \_ Размер буфера постоянного сервера \_<2> предоставляет размер буфера маршалирования в виде предварительно вычисленного компилятором.</span><span class="sxs-lookup"><span data-stu-id="98809-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="98809-171">Это может быть только частичный размер, так как флаг Сервермустсизе инициирует изменение размера.</span><span class="sxs-lookup"><span data-stu-id="98809-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="98809-172">\_Флаги opt интерпретатора \_ определяются в ндртипес. h:</span><span class="sxs-lookup"><span data-stu-id="98809-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="98809-173">Бит Сервермустсизе устанавливается, если серверу необходимо выполнить проход по размерам буфера.</span><span class="sxs-lookup"><span data-stu-id="98809-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="98809-174">Бит Клиентмустсизе устанавливается, если клиенту необходимо выполнить проход по размерам буфера.</span><span class="sxs-lookup"><span data-stu-id="98809-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="98809-175">Бит Хасретурн устанавливается, если процедура имеет возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="98809-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="98809-176">Бит Хаспипес устанавливается, если необходимо использовать пакет канала для поддержки аргумента канала.</span><span class="sxs-lookup"><span data-stu-id="98809-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="98809-177">Бит Хасасинкууид устанавливается, если процедура является асинхронной процедурой DCOM.</span><span class="sxs-lookup"><span data-stu-id="98809-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="98809-178">Бит Хасекстенсионс указывает, что используются расширения Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="98809-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="98809-179">Бит Хасасинчандле указывает асинхронную процедуру RPC.</span><span class="sxs-lookup"><span data-stu-id="98809-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="98809-180">Бит Хасасинчандле изначально использовался в качестве другой реализации модели асинхронной поддержки DCOM, и поэтому не может использоваться для асинхронной поддержки текущего стиля в DCOM.</span><span class="sxs-lookup"><span data-stu-id="98809-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="98809-181">В настоящее время бит Хасасинкууид указывает на это.</span><span class="sxs-lookup"><span data-stu-id="98809-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 