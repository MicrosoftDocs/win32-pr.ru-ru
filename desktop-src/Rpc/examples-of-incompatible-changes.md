---
title: Примеры несовместимых изменений
description: 'При работе с несовместимыми изменениями несвязанное правило Thumb выглядит следующим образом: любое изменение может быть обратно несовместимым, если оно не слишком хорошо понятно.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068129"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="669c5-103">Примеры несовместимых изменений</span><span class="sxs-lookup"><span data-stu-id="669c5-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="669c5-104">При работе с несовместимыми изменениями несвязанное правило Thumb имеет следующий вид: любое изменение может быть обратно несовместимым, если оно не слишком хорошо понятно.</span><span class="sxs-lookup"><span data-stu-id="669c5-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="669c5-105">Это правило требует знания правил NDR.</span><span class="sxs-lookup"><span data-stu-id="669c5-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="669c5-106">Если вы не уверены, что такое NDR, не вносите изменения.</span><span class="sxs-lookup"><span data-stu-id="669c5-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="669c5-107">Примеры изменений, которые обычно приводят к нарушению прав доступа в приложении, или \_ \_ исключением данных заглушки, \_ вызванных модулем упаковки, являются следующие.</span><span class="sxs-lookup"><span data-stu-id="669c5-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="669c5-108">Добавление нового метода в середину старых методов.</span><span class="sxs-lookup"><span data-stu-id="669c5-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="669c5-109">Добавление или удаление параметров из метода.</span><span class="sxs-lookup"><span data-stu-id="669c5-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="669c5-110">Изменение атрибута, например, атрибута указателя: изменение \[ ссылки \] на \[ Unique \] или \[ ptr \] или наоборот.</span><span class="sxs-lookup"><span data-stu-id="669c5-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="669c5-111">Каждый тип указателя имеет другое представление провода.</span><span class="sxs-lookup"><span data-stu-id="669c5-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="669c5-112">Изменение размера данных: с короткого на длинный, от char до WCHAR \_ t (Юникод) Добавление поля в структуру с изменением размера массива фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="669c5-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="669c5-113">Добавление подлокотников Union к объединению с предложением Default.</span><span class="sxs-lookup"><span data-stu-id="669c5-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="669c5-114">Некоторые коварные изменения или непредвиденные несоответствия между клиентом и сервером могут происходить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="669c5-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="669c5-115">Изменение элемента составного типа, например структуры или массива.</span><span class="sxs-lookup"><span data-stu-id="669c5-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="669c5-116">Например, если \_ идентификатор клиента меняется с целочисленного на GUID, \_ Структура записи клиента с \_ полем идентификатор клиента станет несовместимой.</span><span class="sxs-lookup"><span data-stu-id="669c5-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="669c5-117">Это может быть трудно обнаружить в каскадном соединении по нескольким уровням внедрения к фактическому типу удаленного параметра.</span><span class="sxs-lookup"><span data-stu-id="669c5-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="669c5-118">Изменение импортированного типа.</span><span class="sxs-lookup"><span data-stu-id="669c5-118">Modifying an imported type.</span></span> <span data-ttu-id="669c5-119">Тип может быть получен из другого компонента, который не является удаленным напрямую, поэтому изменение было считалось совместимым.</span><span class="sxs-lookup"><span data-stu-id="669c5-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="669c5-120">Использование \# ifdef в IDL-файле является неправильной идеей определений типа ifdef в IDL-файле — это аварийное завершение.</span><span class="sxs-lookup"><span data-stu-id="669c5-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="669c5-121">Неизбежно, из-за сборки или других сбоев, клиент компилируется с другим набором определений, чем сервер, и в итоге они несовместимы.</span><span class="sxs-lookup"><span data-stu-id="669c5-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




