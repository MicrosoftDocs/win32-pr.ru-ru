---
title: Массивы и указатели
description: Удаленный вызов процедур (RPC) в основном является прозрачным для разработчиков.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Удаленный вызов процедур RPC, описание, массивы и указатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776871"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="ff4ce-104">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="ff4ce-104">Arrays and Pointers</span></span>

<span data-ttu-id="ff4ce-105">Удаленный вызов процедур (RPC) в основном является прозрачным для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="ff4ce-106">Для достижения этой прозрачности клиентская заглушка передает на сервер как указатель, так и объект данных, на который он указывает.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="ff4ce-107">Если удаленная процедура изменяет данные, сервер должен передать новые данные обратно клиенту, чтобы клиент мог скопировать новые данные по исходным данным.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="ff4ce-108">Как правило, удаленный вызов процедуры ведет себя так же, как вызов локальной процедуры.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="ff4ce-109">То есть, если указатель является параметром, то Удаленная процедура может получить доступ к объекту данных, на который ссылается указатель, так же, как это может делать локальная процедура.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="ff4ce-110">Поскольку клиентские и серверные программы выполняются в разных адресных пространствах, разработчики должны использовать атрибуты язык MIDL (MIDL) для описания передачи данных массива и указателя между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ff4ce-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="ff4ce-111">В этом разделе представлен обзор использования массивов и указателей в распределенных приложениях в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ff4ce-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="ff4ce-112">Массивы и RPC</span><span class="sxs-lookup"><span data-stu-id="ff4ce-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="ff4ce-113">Указатели и RPC</span><span class="sxs-lookup"><span data-stu-id="ff4ce-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="ff4ce-114">Использование массивов, строк и указателей</span><span class="sxs-lookup"><span data-stu-id="ff4ce-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




