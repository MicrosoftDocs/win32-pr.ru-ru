---
title: Расширения Microsoft RPC Binding-Handle
description: Расширения Майкрософт для языка IDL поддерживают несколько параметров обработки, которые отображаются в позициях, отличных от первого, крайнего левого, параметра.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104070767"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="a2345-103">Расширения Microsoft RPC Binding-Handle</span><span class="sxs-lookup"><span data-stu-id="a2345-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="a2345-104">Расширения Майкрософт для языка IDL поддерживают несколько параметров обработки, которые отображаются в позициях, отличных от первого, крайнего левого, параметра.</span><span class="sxs-lookup"><span data-stu-id="a2345-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="a2345-105">Следующие шаги описывают последовательность, с которой компилятор MIDL проходит, чтобы разрешить параметр Binding-Handle в режиме совместимости DCE (/**Использование**) и в режиме по умолчанию (Расширенный Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="a2345-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="a2345-106">Режим совместимости DCE</span><span class="sxs-lookup"><span data-stu-id="a2345-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="a2345-107">Маркер привязки, который отображается в первой позицией.</span><span class="sxs-lookup"><span data-stu-id="a2345-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="a2345-108">Крайний левый \[ [**в**](/windows/desktop/Midl/in)параметре [**\_ обработчика контекста**](/windows/desktop/Midl/context-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="a2345-109">Неявный маркер привязки, заданный \[ [**неявным \_ обработчиком**](/windows/desktop/Midl/implicit-handle) \] или \[ [**автоматическим \_ обработчиком**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="a2345-110">Если ACF отсутствует, по умолчанию используется \[ **Автоматический \_ обработчик** \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="a2345-111">Режим по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a2345-111">Default mode</span></span>

-   <span data-ttu-id="a2345-112">Крайний слева явный маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="a2345-113">Неявный маркер привязки, заданный \[ [**неявным \_ обработчиком**](/windows/desktop/Midl/implicit-handle) \] или \[ [**автоматическим \_ обработчиком**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="a2345-114">Если ACF отсутствует, по умолчанию используется \[ [**Автоматический \_ обработчик**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a2345-115">Компиляторы DCE IDL ищут явный маркер привязки в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="a2345-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="a2345-116">Если первый параметр не является дескриптором привязки и указаны один или несколько дескрипторов контекста, то в качестве дескриптора привязки используется крайний левый дескриптор контекста.</span><span class="sxs-lookup"><span data-stu-id="a2345-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="a2345-117">Если первый параметр не является дескриптором и дескрипторы контекста отсутствуют, процедура использует неявную привязку с помощью \[ [**неявного \_ дескриптора**](/windows/desktop/Midl/implicit-handle) \] или \[ [**автоматической \_ обработки**](/windows/desktop/Midl/auto-handle)атрибута ACF \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a2345-118">Расширения Майкрософт для IDL позволяют использовать маркер привязки в месте, отличном от первого параметра.</span><span class="sxs-lookup"><span data-stu-id="a2345-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="a2345-119">Крайний левый \[ [**в**](/windows/desktop/Midl/in) \] параметре явного обработчика — является ли он примитивом, определяемым программистом или маркером контекста — является маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="a2345-120">При отсутствии параметров обработки процедура использует неявную привязку с помощью \[ [**неявного \_ обработчика**](/windows/desktop/Midl/implicit-handle) атрибута ACF \] или \[ [**автоматической \_ обработки**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="a2345-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a2345-121">Следующие правила применяются как к режиму DCE-совместимости (/ОСФ), так и к режиму по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a2345-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="a2345-122">Привязка с автоматической обработкой используется, когда отсутствует ACF.</span><span class="sxs-lookup"><span data-stu-id="a2345-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="a2345-123">Явные \[ [](/windows/desktop/Midl/in) \] дескрипторы in или \[ **in** [**out**](/windows/desktop/Midl/out-idl) \] для отдельной функции загружают любую неявную привязку, заданную для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a2345-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="a2345-124">\[Не поддерживаются несколько [**входных**](/windows/desktop/Midl/in) \] и входных \[  \] дескрипторов-примитивов.</span><span class="sxs-lookup"><span data-stu-id="a2345-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="a2345-125">\[ [](/windows/desktop/Midl/in) \] \[  \] Разрешено использовать несколько дескрипторов явного контекста в или в.</span><span class="sxs-lookup"><span data-stu-id="a2345-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="a2345-126">Все определяемые программистом параметры обработки, за исключением параметра Binding-Handle, рассматриваются как трансмиссибле данные.</span><span class="sxs-lookup"><span data-stu-id="a2345-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="a2345-127">Следующая таблица содержит примеры и описывает назначение дескрипторов привязки в каждом режиме компилятора.</span><span class="sxs-lookup"><span data-stu-id="a2345-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2345-128">Пример</span><span class="sxs-lookup"><span data-stu-id="a2345-128">Example</span></span></th>
<th><span data-ttu-id="a2345-129">Описание</span><span class="sxs-lookup"><span data-stu-id="a2345-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="a2345-130">Явный маркер не задан.</span><span class="sxs-lookup"><span data-stu-id="a2345-130">No explicit handle is specified.</span></span> <span data-ttu-id="a2345-131">Используется неявный маркер привязки, заданный параметром [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] или [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>].</span><span class="sxs-lookup"><span data-stu-id="a2345-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="a2345-132">Если ACF отсутствует, используется автоматический обработчик.</span><span class="sxs-lookup"><span data-stu-id="a2345-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="a2345-133">Указан явный обработчик типа handle_t.</span><span class="sxs-lookup"><span data-stu-id="a2345-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="a2345-134">Параметр <em>H</em> является маркером привязки для процедуры.</span><span class="sxs-lookup"><span data-stu-id="a2345-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="a2345-135">Первый параметр не является обработчиком.</span><span class="sxs-lookup"><span data-stu-id="a2345-135">The first parameter is not a handle.</span></span> <span data-ttu-id="a2345-136">В режиме по умолчанию левый параметр Handle ( <em>H</em>) является маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="a2345-137">В режиме/ОСФ используется неявная привязка.</span><span class="sxs-lookup"><span data-stu-id="a2345-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="a2345-138">Сообщается об ошибке, так как второй параметр должен быть трансмиссибле, а handle_t передаваться.</span><span class="sxs-lookup"><span data-stu-id="a2345-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="a2345-139">Первый параметр не является обработчиком.</span><span class="sxs-lookup"><span data-stu-id="a2345-139">The first parameter is not a handle.</span></span> <span data-ttu-id="a2345-140">В режиме по умолчанию левый параметр Handle ( <em>H</em>) является маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="a2345-141">Заглушки вызывают предоставляемые пользователем подпрограммы MY_HDL_bind и MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="a2345-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="a2345-142">В режиме "в/использование" используется неявная привязка.</span><span class="sxs-lookup"><span data-stu-id="a2345-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="a2345-143">Параметр обработки <em>H</em> , определяемый программистом, обрабатывается как трансмиссибле данные.</span><span class="sxs-lookup"><span data-stu-id="a2345-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="a2345-144">Первый параметр — это маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="a2345-145">Параметр <em>H</em> является параметром обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="a2345-146">Второй определяемый программистом параметр Handle обрабатывается как данные трансмиссибле.</span><span class="sxs-lookup"><span data-stu-id="a2345-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="a2345-147">Маркер привязки — это контекстный обработчик.</span><span class="sxs-lookup"><span data-stu-id="a2345-147">The binding handle is a context handle.</span></span> <span data-ttu-id="a2345-148">Параметр <em>H</em> является маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="a2345-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 