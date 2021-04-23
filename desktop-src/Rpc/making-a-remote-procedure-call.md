---
title: Выполнение удаленного вызова процедур
description: После того как клиентская программа распределенных приложений, использующих явные дескрипторы привязки, имеет дескриптор привязки, она может выполнять удаленные процедуры.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Удаленный вызов процедур RPC, задачи, выполнение вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772719"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="0eaa6-104">Выполнение удаленного вызова процедур</span><span class="sxs-lookup"><span data-stu-id="0eaa6-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="0eaa6-105">После того как клиентская программа распределенных приложений, использующих явные дескрипторы привязки, имеет дескриптор привязки, она может выполнять удаленные процедуры.</span><span class="sxs-lookup"><span data-stu-id="0eaa6-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="0eaa6-106">Microsoft RPC также предлагает пользовательские дескрипторы привязки, неявные дескрипторы привязки и автоматические маркеры привязки.</span><span class="sxs-lookup"><span data-stu-id="0eaa6-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="0eaa6-107">Эти дескрипторы привязки предоставляют клиентским и серверным программам различные уровни управления процессом выполнения удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="0eaa6-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="0eaa6-108">Дополнительные сведения о различных типах дескрипторов и гибкости, которые они предлагают, см. в разделе [Binding and Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0eaa6-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="0eaa6-109">Чтобы выполнить вызов процедуры удаленно, вызовите клиентскую функцию-заглушку так же, как и любую функцию C.</span><span class="sxs-lookup"><span data-stu-id="0eaa6-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




