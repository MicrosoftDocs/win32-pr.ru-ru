---
title: Прокси-файл интерфейса
description: Прокси-файл интерфейса (U \_ p. c) — это файл c, который содержит подпрограммы, эквивалентные параметрам в заглушках клиента и серверам-заглушках интерфейса Object (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL и COM MIDL, интерфейсы, прокси-файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986663"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="7c472-104">Прокси-файл интерфейса</span><span class="sxs-lookup"><span data-stu-id="7c472-104">The Interface Proxy File</span></span>

<span data-ttu-id="7c472-105">Прокси-файл интерфейса (U \_ p. c) — это файл c, который содержит подпрограммы, эквивалентные параметрам в заглушках клиента и серверам-заглушках интерфейса Object (com).</span><span class="sxs-lookup"><span data-stu-id="7c472-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="7c472-106">Этот файл содержит реализации суррогатных подпрограмм для клиента и сервера во встроенном режиме компилятора или эквивалентных данных и преобразователей в интерпретируемых режимах, а также других соответствующих связующих данных COM, таких как прокси-серверы и заглушки.</span><span class="sxs-lookup"><span data-stu-id="7c472-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="7c472-107">Файл прокси-сервера интерфейса включает вспомогательные подпрограммы и данные только для методов интерфейсов, определенных в текущем IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="7c472-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="7c472-108">Чтобы объяснить это поведение, в этом разделе используется расширенный пример.</span><span class="sxs-lookup"><span data-stu-id="7c472-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="7c472-109">При компиляции IDL-файла с интерфейсом, таким как Ифацеб, который наследуется от Ифацеа, Ифацеб связанные вспомогательные данные и подпрограммы генерируются для текущего прокси-файла, а базовый интерфейс Ифацеа связанные вспомогательные данные и подпрограммы находятся в прокси, созданном на основе файла IDL, содержащего определение Ифацеа.</span><span class="sxs-lookup"><span data-stu-id="7c472-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="7c472-110">Компилятор создает все данные, необходимые для указания суррогатов базового интерфейса, и делегирует их при необходимости для поддержки методов Ифацеа, используемых через интерфейс Ифацеб.</span><span class="sxs-lookup"><span data-stu-id="7c472-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="7c472-111">Для каждого метода в интерфейсе в текущем IDL-файле файл прокси содержит следующие два суррогатных метода при компиляции в смешанном режиме ([/OS](-os.md)) и эквивалентные данные интерпретатора при компиляции в режиме интерпретатора ([/Oi](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="7c472-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="7c472-112">Суррогат на стороне клиента, например \_ прокси метода ифацеб \_ в этом примере.</span><span class="sxs-lookup"><span data-stu-id="7c472-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="7c472-113">Этот суррогат на стороне клиента — это виртуальная точка входа, в которую клиент, например Ифацеб:: Method, отправляется.</span><span class="sxs-lookup"><span data-stu-id="7c472-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="7c472-114">Он маршалирует входные аргументы в передаваемые формы, передает Упакованные аргументы вместе со сведениями, идентифицирующими интерфейс и операцию, а затем демаршалирует возвращаемое значение и любые выходные аргументы при возвращении вызванной операции.</span><span class="sxs-lookup"><span data-stu-id="7c472-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="7c472-115">Суррогат на стороне сервера, например \_ \_ заглушка метода ифацеб.</span><span class="sxs-lookup"><span data-stu-id="7c472-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="7c472-116">Этот суррогат на стороне сервера — это виртуальная точка входа, которую отправляются базовой средой выполнения на сервер для эмуляции клиента.</span><span class="sxs-lookup"><span data-stu-id="7c472-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="7c472-117">Он выполняет детрансляцию входных аргументов для репликации клиентских данных, вызывает реализацию функции интерфейса сервера, а затем маршалирует и передает возвращаемое значение и все выходные аргументы обратно на клиентскую сторону.</span><span class="sxs-lookup"><span data-stu-id="7c472-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="7c472-118">Имя по умолчанию для прокси-файла, созданного из файла. idl, — это файл \_ p. c. Используйте параметр компилятора [**/proxy**](-proxy.md) MIDL, чтобы переопределить имя по умолчанию для файла прокси интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7c472-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="7c472-119">Параметры [**/env**](-env.md) и [**/out**](-out.md) влияют на этот файл.</span><span class="sxs-lookup"><span data-stu-id="7c472-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




