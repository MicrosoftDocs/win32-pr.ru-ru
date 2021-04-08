---
title: Типы дескрипторов привязки
description: Дескрипторы привязки могут быть автоматическими, неявными или явно.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068336"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="2c258-103">Типы дескрипторов привязки</span><span class="sxs-lookup"><span data-stu-id="2c258-103">Types of Binding Handles</span></span>

<span data-ttu-id="2c258-104">Дескрипторы привязки могут быть автоматическими, неявными или явно.</span><span class="sxs-lookup"><span data-stu-id="2c258-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="2c258-105">Они отличаются от объема контроля над процессом привязки в приложении.</span><span class="sxs-lookup"><span data-stu-id="2c258-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="2c258-106">Как видно из названия, автоматические дескрипторы привязки автоматизируют привязку.</span><span class="sxs-lookup"><span data-stu-id="2c258-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="2c258-107">Клиентским и серверным приложениям не требуется код для обработки процесса привязки.</span><span class="sxs-lookup"><span data-stu-id="2c258-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="2c258-108">Неявные дескрипторы привязки позволяют клиентским программам настраивать дескриптор привязки до того, как будет выполнена привязка.</span><span class="sxs-lookup"><span data-stu-id="2c258-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="2c258-109">После того как клиент установит привязку, Библиотека времени выполнения RPC будет обрабатывать остальные компоненты.</span><span class="sxs-lookup"><span data-stu-id="2c258-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="2c258-110">Явные дескрипторы привязки полностью контролируют процесс привязки в исходном коде клиента и серверных программ.</span><span class="sxs-lookup"><span data-stu-id="2c258-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="2c258-111">Благодаря этому элементу управления повышается сложность.</span><span class="sxs-lookup"><span data-stu-id="2c258-111">With this control comes increased complexity.</span></span> <span data-ttu-id="2c258-112">Приложение должно вызывать функции RPC для управления привязкой.</span><span class="sxs-lookup"><span data-stu-id="2c258-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="2c258-113">Это не происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="2c258-113">It does not happen automatically.</span></span> <span data-ttu-id="2c258-114">Рекомендуется использовать явные дескрипторы привязки.</span><span class="sxs-lookup"><span data-stu-id="2c258-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="2c258-115">На следующей схеме показаны различия между автоматическим, неявным и явно заданными дескрипторами привязки.</span><span class="sxs-lookup"><span data-stu-id="2c258-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![различия между автоматическим, неявным и явно заданными дескрипторами привязки](images/bhand.png)

<span data-ttu-id="2c258-117">Кроме того, каждый маркер привязки может быть простым или пользовательским.</span><span class="sxs-lookup"><span data-stu-id="2c258-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="2c258-118">Каждый тип маркера привязки рассматривается в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2c258-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="2c258-119">Автоматические маркеры привязки</span><span class="sxs-lookup"><span data-stu-id="2c258-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="2c258-120">Неявные дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="2c258-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="2c258-121">Явные дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="2c258-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="2c258-122">Простые и пользовательские дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="2c258-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




