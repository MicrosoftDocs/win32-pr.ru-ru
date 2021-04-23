---
title: Функция type_UserSize
description: Функция Type \_ усерсизе — это вспомогательная функция для атрибутов \ "\ проводное \_ маршалирование \" и \ "пользовательское \_ маршалирование \".
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793663"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="62baa-104">Тип \_ Усерсизе функция</span><span class="sxs-lookup"><span data-stu-id="62baa-104">The type\_UserSize Function</span></span>

<span data-ttu-id="62baa-105">Функция **<type> \_ усерсизе** является вспомогательной функцией для \[ атрибутов [ \_ маршалирования](/windows/desktop/Midl/wire-marshal) \] и \[ [ \_ маршалирования пользователя](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="62baa-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="62baa-106">Заглушки вызывают эту функцию для изменения размера буфера данных RPC для объекта данных пользователя перед упаковкой данных на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="62baa-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="62baa-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62baa-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="62baa-108"><type>В имени функции — это усерм-тип, как указано в определении типа " **\[ проводное \_ маршалирование \]** " или " **\[ пользовательское \_ маршалирование \]** ".</span><span class="sxs-lookup"><span data-stu-id="62baa-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="62baa-109">Этот тип может быть непригодным или даже при использовании с атрибутом **\[ пользовательской \_ маршалирования \]** , неизвестным компилятору MIDL.</span><span class="sxs-lookup"><span data-stu-id="62baa-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="62baa-110">Имя типа провода (имя типа, переданного по сети) не используется в прототипе функции.</span><span class="sxs-lookup"><span data-stu-id="62baa-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="62baa-111">Однако обратите внимание, что тип провода определяет макет для данных, как указано в использование DCE.</span><span class="sxs-lookup"><span data-stu-id="62baa-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="62baa-112">Все данные должны быть преобразованы в формат представления данных сети (NDR).</span><span class="sxs-lookup"><span data-stu-id="62baa-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="62baa-113">Параметр *пфлагс* является указателем на **беззнаковое поле с длинным** флагом.</span><span class="sxs-lookup"><span data-stu-id="62baa-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="62baa-114">Верхнее слово флага содержит флаги формата NDR в соответствии с определением использование DCE для чисел с плавающей запятой, порядка байтов и символьных представлений.</span><span class="sxs-lookup"><span data-stu-id="62baa-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="62baa-115">В нижнем слове содержится флаг контекста маршалирования, определенный в канале COM.</span><span class="sxs-lookup"><span data-stu-id="62baa-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="62baa-116">Точная структура флагов в поле показана в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62baa-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="62baa-117">Bits</span><span class="sxs-lookup"><span data-stu-id="62baa-117">Bits</span></span>  | <span data-ttu-id="62baa-118">Флаг</span><span class="sxs-lookup"><span data-stu-id="62baa-118">Flag</span></span>                                  | <span data-ttu-id="62baa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="62baa-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62baa-120">31-24</span><span class="sxs-lookup"><span data-stu-id="62baa-120">31-24</span></span> | <span data-ttu-id="62baa-121">Представление с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="62baa-121">Floating-point representation</span></span>         | <span data-ttu-id="62baa-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="62baa-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="62baa-123">23-20</span><span class="sxs-lookup"><span data-stu-id="62baa-123">23-20</span></span> | <span data-ttu-id="62baa-124">Последовательность байтов и чисел с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="62baa-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="62baa-125">0 = Big с обратным порядком байтов 1 = с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="62baa-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="62baa-126">19-16</span><span class="sxs-lookup"><span data-stu-id="62baa-126">19-16</span></span> | <span data-ttu-id="62baa-127">Символьное представление</span><span class="sxs-lookup"><span data-stu-id="62baa-127">Character representation</span></span>              | <span data-ttu-id="62baa-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="62baa-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="62baa-129">15-0</span><span class="sxs-lookup"><span data-stu-id="62baa-129">15-0</span></span>  | <span data-ttu-id="62baa-130">Флаг контекста маршалирования</span><span class="sxs-lookup"><span data-stu-id="62baa-130">Marshaling context flag</span></span>               | <span data-ttu-id="62baa-131">0 = МШКТКС \_ Local 1 = мшкткс \_ ношаредмем 2 = мшкткс \_ ДИФФЕРЕНТМАЧИНЕ 3 = мшкткс \_ INPROC</span><span class="sxs-lookup"><span data-stu-id="62baa-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="62baa-132">Флаг контекста маршалинга позволяет изменить поведение подпрограммы в зависимости от контекста вызова RPC.</span><span class="sxs-lookup"><span data-stu-id="62baa-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="62baa-133">Например, если имеется маркер (**Long**) для блока данных, то можно отправить маркер для внутрипроцессного вызова, но фактические данные будут отправлены для вызова на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="62baa-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="62baa-134">Флаг контекста маршалирования и его значения определены в файлах Втипес. h и Втипес. idl в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="62baa-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="62baa-135">Если тип провода определен правильно, нет необходимости использовать флаги формата NDR, так как модуль NDR выполняет необходимые преобразования.</span><span class="sxs-lookup"><span data-stu-id="62baa-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="62baa-136">Параметр *стартингсизе* , который является текущим смещением буфера.</span><span class="sxs-lookup"><span data-stu-id="62baa-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="62baa-137">Начальный размер указывает смещение буфера для объекта пользователя, а также может быть неправильно согласовано.</span><span class="sxs-lookup"><span data-stu-id="62baa-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="62baa-138">Ваша подпрограммы должна учитывать все необходимое заполнение.</span><span class="sxs-lookup"><span data-stu-id="62baa-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="62baa-139">Параметр *пмйобж* является указателем на объект пользовательского типа.</span><span class="sxs-lookup"><span data-stu-id="62baa-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="62baa-140">Возвращаемое значение — это новое смещение или позиция буфера.</span><span class="sxs-lookup"><span data-stu-id="62baa-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="62baa-141">Функция должна возвращать совокупный размер, который является начальным размером, а также возможным заполнением и размером данных.</span><span class="sxs-lookup"><span data-stu-id="62baa-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="62baa-142">Функция **<type> \_ усерсизе** может возвращать переоценку требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="62baa-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="62baa-143">Фактический размер буфера отправки определяется размером данных, а не размером выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="62baa-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="62baa-144">Функция **<type> \_ усерсизе** не вызывается, если размер сети можно вычислить во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="62baa-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="62baa-145">Обратите внимание, что для большинства объединений, даже если нет указателей, фактический размер представления подключения можно определить только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="62baa-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62baa-146">См. также</span><span class="sxs-lookup"><span data-stu-id="62baa-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62baa-147">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="62baa-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="62baa-148">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="62baa-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="62baa-149">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="62baa-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 