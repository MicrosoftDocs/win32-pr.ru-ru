---
title: Компоненты RPC
description: Компоненты удаленного вызова процедур (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Удаленный вызов процедур RPC, описание, компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986530"
---
# <a name="rpc-components"></a><span data-ttu-id="390e0-104">Компоненты RPC</span><span class="sxs-lookup"><span data-stu-id="390e0-104">RPC Components</span></span>

<span data-ttu-id="390e0-105">RPC включает следующие основные компоненты:</span><span class="sxs-lookup"><span data-stu-id="390e0-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="390e0-106">Компилятор MIDL</span><span class="sxs-lookup"><span data-stu-id="390e0-106">MIDL compiler</span></span>
-   <span data-ttu-id="390e0-107">Библиотеки времени выполнения и файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="390e0-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="390e0-108">Поставщик службы имен (иногда называемый указателем)</span><span class="sxs-lookup"><span data-stu-id="390e0-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="390e0-109">Сопоставитель конечных точек (иногда называемый средством сопоставления портов)</span><span class="sxs-lookup"><span data-stu-id="390e0-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="390e0-110">В модели RPC можно формально указать интерфейс для удаленных процедур с помощью языка, предназначенного для этой цели.</span><span class="sxs-lookup"><span data-stu-id="390e0-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="390e0-111">Этот язык называется языком определения интерфейса или IDL.</span><span class="sxs-lookup"><span data-stu-id="390e0-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="390e0-112">Реализация этого языка корпорацией Майкрософт называется язык MIDL или MIDL.</span><span class="sxs-lookup"><span data-stu-id="390e0-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="390e0-113">После создания интерфейса его необходимо передать через компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="390e0-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="390e0-114">Этот компилятор создает заглушки, которые преобразуют вызовы локальных процедур в удаленные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="390e0-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="390e0-115">Заглушки — это функции-заполнители, которые выполняют вызовы функций библиотеки времени выполнения, которые управляют удаленным вызовом процедур.</span><span class="sxs-lookup"><span data-stu-id="390e0-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="390e0-116">Преимущество такого подхода заключается в том, что сеть становится почти полностью прозрачной для распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="390e0-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="390e0-117">Клиентская программа вызывает то, что кажется локальными процедурами; работа по их преобразованию в удаленные вызовы выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="390e0-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="390e0-118">Весь код, который преобразует данные, обращается к сети и получает результаты, создается компилятором MIDL и является невидимым для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="390e0-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




