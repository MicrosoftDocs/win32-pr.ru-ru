---
title: Интерфейсы в распределенных объектах
description: В распределенных вычислениях интерфейс представляет собой коллекцию определений и удаленных функций, которые позволяют двум или более программам взаимодействовать между различными контекстами.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- интерфейсы MIDL в распределенных объектах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337284"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="56c52-104">Интерфейсы в распределенных объектах</span><span class="sxs-lookup"><span data-stu-id="56c52-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="56c52-105">В распределенных вычислениях интерфейс представляет собой коллекцию определений и удаленных функций, которые позволяют двум или более программам взаимодействовать между различными контекстами.</span><span class="sxs-lookup"><span data-stu-id="56c52-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="56c52-106">В приложении RPC интерфейс указывает:</span><span class="sxs-lookup"><span data-stu-id="56c52-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="56c52-107">Как клиентские и серверные приложения идентифицируют себя друг с другом.</span><span class="sxs-lookup"><span data-stu-id="56c52-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="56c52-108">Передача данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="56c52-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="56c52-109">Удаленные процедуры, которые может вызывать клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="56c52-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="56c52-110">Типы данных для параметров и возвращаемых значений удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="56c52-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="56c52-111">Язык MIDL (MIDL) предназначен для реализации интерфейсов, используемых в распределенных приложениях.</span><span class="sxs-lookup"><span data-stu-id="56c52-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="56c52-112">С помощью MIDL приложение может иметь один или несколько интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="56c52-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="56c52-113">Каждый интерфейс указывает уникальный распределенный контракт между программами клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="56c52-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="56c52-114">Приложения, основанные на удаленных вызовах процедур (RPC), модели COM и распределенных объектных моделях компонентов (DCOM), определяют свои интерфейсы с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="56c52-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="56c52-115">MIDL напоминает C и C++ различными способами.</span><span class="sxs-lookup"><span data-stu-id="56c52-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="56c52-116">Общие сведения о создании интерфейсов MIDL см. [в разделе Разработка интерфейса](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="56c52-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 