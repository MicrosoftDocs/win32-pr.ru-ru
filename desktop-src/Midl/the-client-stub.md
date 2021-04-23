---
title: Клиентская заглушка
description: Модуль-заглушка клиента предоставляет суррогатные точки входа на клиент для каждой операции, определенной во входном IDL-файле.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL и RPC MIDL, интерфейсы, заглушка клиента
- интерфейс MIDL
- интерфейсы MIDL, MIDL и RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331376"
---
# <a name="the-client-stub"></a><span data-ttu-id="ac67b-106">Клиентская заглушка</span><span class="sxs-lookup"><span data-stu-id="ac67b-106">The Client Stub</span></span>

<span data-ttu-id="ac67b-107">Модуль-заглушка клиента предоставляет суррогатные точки входа на клиент для каждой операции, определенной во входном IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="ac67b-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="ac67b-108">Когда клиентское приложение выполняет вызов удаленной процедуры, его вызов сначала перемещается в подпрограмму-суррогат в файле заглушки клиента.</span><span class="sxs-lookup"><span data-stu-id="ac67b-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="ac67b-109">Подпрограммная заглушка клиента выполняет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="ac67b-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="ac67b-110">Маршалирует аргументы.</span><span class="sxs-lookup"><span data-stu-id="ac67b-110">Marshals arguments.</span></span> <span data-ttu-id="ac67b-111">Клиентская заглушка упаковывает входные аргументы в форму, которая может быть передана на сервер.</span><span class="sxs-lookup"><span data-stu-id="ac67b-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="ac67b-112">Вызывает библиотеку времени выполнения клиента для передачи аргументов в удаленное адресное пространство и вызывает удаленную процедуру в адресном пространстве сервера.</span><span class="sxs-lookup"><span data-stu-id="ac67b-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="ac67b-113">Распаковать выходные аргументы.</span><span class="sxs-lookup"><span data-stu-id="ac67b-113">Unmarshals output arguments.</span></span> <span data-ttu-id="ac67b-114">Заглушка клиента распаковать выходные аргументы и вернет их вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="ac67b-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="ac67b-115">Компилятор MIDL переключает [**/Client**](-client.md), [**/cstub**](-cstub.md)и [**/out**](-out.md) на файл заглушки клиента.</span><span class="sxs-lookup"><span data-stu-id="ac67b-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




