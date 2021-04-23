---
title: Заглушка сервера
description: Заглушка сервера предоставляет суррогатные точки входа на сервере для каждой операции, определенной во входном IDL-файле.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL-компилятор MIDL, MIDL и RPC MIDL, интерфейсы, заглушка сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068408"
---
# <a name="the-server-stub"></a><span data-ttu-id="da9b7-104">Заглушка сервера</span><span class="sxs-lookup"><span data-stu-id="da9b7-104">The Server Stub</span></span>

<span data-ttu-id="da9b7-105">Заглушка сервера предоставляет суррогатные точки входа на сервере для каждой операции, определенной во входном IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="da9b7-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="da9b7-106">При вызове подпрограммы-заглушки сервера с помощью библиотеки времени выполнения RPC, она выполняет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="da9b7-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="da9b7-107">Распаковать входные аргументы (распаковать аргументы из переданных форматов).</span><span class="sxs-lookup"><span data-stu-id="da9b7-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="da9b7-108">Вызывает фактическую реализацию процедуры на сервере.</span><span class="sxs-lookup"><span data-stu-id="da9b7-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="da9b7-109">Маршалирует выходные аргументы (упаковывает аргументы в передаваемые формы).</span><span class="sxs-lookup"><span data-stu-id="da9b7-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="da9b7-110">Компилятор MIDL переключает параметры [**/Server**](-server.md), [**/sstub**](-sstub.md)и [**/out**](-out.md) на файл заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="da9b7-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




