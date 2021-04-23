---
title: Дескрипторы привязки MIDL
description: Дескрипторы привязки — это объекты данных, представляющие привязку между клиентом и сервером.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- типы данных MIDL, дескрипторы привязки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069836"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="2a4d0-104">Дескрипторы привязки MIDL</span><span class="sxs-lookup"><span data-stu-id="2a4d0-104">MIDL Binding Handles</span></span>

<span data-ttu-id="2a4d0-105">Дескрипторы привязки — это объекты данных, представляющие привязку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="2a4d0-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="2a4d0-106">MIDL поддерживает базовый тип [**маркера \_ t**](handle-t.md).</span><span class="sxs-lookup"><span data-stu-id="2a4d0-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="2a4d0-107">Дескрипторы этого типа называются "примитивными дескрипторами".</span><span class="sxs-lookup"><span data-stu-id="2a4d0-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="2a4d0-108">Вы можете определить собственные типы обработчиков с помощью атрибута **\[ Handle \]** .</span><span class="sxs-lookup"><span data-stu-id="2a4d0-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="2a4d0-109">Дескрипторы, определенные таким образом, называются "определяемыми пользователем", "настроенными" или "универсальными" дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="2a4d0-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="2a4d0-110">Можно также определить обработчик, который хранит сведения о состоянии с помощью **\[** [**атрибута \_ Handle контекста**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2a4d0-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="2a4d0-111">Дескрипторы, определенные таким образом, называются дескрипторами "контекста".</span><span class="sxs-lookup"><span data-stu-id="2a4d0-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="2a4d0-112">Если сведения о состоянии не требуются и вы не намерены вызывать библиотеки времени выполнения RPC для управления маркером, вы можете запросить, чтобы библиотеки времени выполнения предработали автоматическую привязку.</span><span class="sxs-lookup"><span data-stu-id="2a4d0-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="2a4d0-113">Это делается с помощью **\[** [**\_ автомаркера**](auto-handle.md)ключевого слова ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="2a4d0-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="2a4d0-114">Можно указать глобальную переменную в качестве маркера привязки с помощью **\[** [**неявного \_ обработчика**](implicit-handle.md)ключевого слова ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="2a4d0-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="2a4d0-115">Ключевое слово **\[ explicit \_ Handle \]** используется, чтобы указать, что каждая Удаленная функция имеет явно заданный обработчик.</span><span class="sxs-lookup"><span data-stu-id="2a4d0-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="2a4d0-116">Дополнительные сведения см. в разделе [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="2a4d0-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 