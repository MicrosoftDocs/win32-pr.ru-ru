---
title: Дескрипторы привязки
description: Привязка — это процесс создания логического соединения между клиентской программой и серверной программой. Сведения, составляющие привязку между клиентом и сервером, представлены структурой, которая называется маркером привязки.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533233"
---
# <a name="binding-handles"></a><span data-ttu-id="78f31-104">Дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="78f31-104">Binding Handles</span></span>

<span data-ttu-id="78f31-105">Привязка — это процесс создания логического соединения между клиентской программой и серверной программой.</span><span class="sxs-lookup"><span data-stu-id="78f31-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="78f31-106">Сведения, составляющие привязку между клиентом и сервером, представлены структурой, которая называется маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="78f31-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="78f31-107">Маркер привязки аналогичен файлу, возвращаемому функцией библиотеки времени выполнения fopen языка C, или обработчику окна, возвращаемому функцией [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="78f31-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="78f31-108">Как и в случае с этими дескрипторами, приложение не может напрямую обращаться к информации в дескрипторе привязки и управлять ею.</span><span class="sxs-lookup"><span data-stu-id="78f31-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="78f31-109">Сведения в структуре данных обработчика привязки доступны только в библиотеках времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="78f31-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="78f31-110">Вы предоставляете обработчик, библиотеки времени выполнения обращаются к соответствующим данным и манипулирует ими.</span><span class="sxs-lookup"><span data-stu-id="78f31-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="78f31-111">В этом разделе представлено обсуждение дескрипторов привязки в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="78f31-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="78f31-112">Типы дескрипторов привязки</span><span class="sxs-lookup"><span data-stu-id="78f31-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="78f31-113">Привязка на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="78f31-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="78f31-114">Привязка на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="78f31-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="78f31-115">Полностью и частично привязанные дескрипторы</span><span class="sxs-lookup"><span data-stu-id="78f31-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="78f31-116">Анализ сведений о привязке</span><span class="sxs-lookup"><span data-stu-id="78f31-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="78f31-117">Расширения Microsoft RPC Binding-Handle</span><span class="sxs-lookup"><span data-stu-id="78f31-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="78f31-118">Функции-обработчики привязки</span><span class="sxs-lookup"><span data-stu-id="78f31-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="78f31-119">База данных службы имен RPC</span><span class="sxs-lookup"><span data-stu-id="78f31-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 