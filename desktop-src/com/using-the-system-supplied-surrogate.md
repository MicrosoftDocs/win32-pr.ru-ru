---
title: Использование суррогата System-Supplied
description: Использование суррогата System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332480"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="2ab20-103">Использование суррогата System-Supplied</span><span class="sxs-lookup"><span data-stu-id="2ab20-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="2ab20-104">Чтобы использовать заданный системой суррогат для сервера DLL, зарегистрируйте библиотеку DLL, указав пустую строку или значение **null** для значения [дллсуррогате](dllsurrogate.md) в реестре.</span><span class="sxs-lookup"><span data-stu-id="2ab20-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="2ab20-105">Когда запрос на активацию для сервера DLL, обозначенный как назначенный COM-серверу, COM запускает процесс суррогата по умолчанию и запрашиваемую библиотеку DLL (указав идентификатор CLSID в командной строке запуска), чтобы избежать отдельного вызова.</span><span class="sxs-lookup"><span data-stu-id="2ab20-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="2ab20-106">(Дополнительные сведения о запуске более чем одного сервера DLL в суррогатном процессе см. в разделе [общий доступ к суррогатам](surrogate-sharing.md)).</span><span class="sxs-lookup"><span data-stu-id="2ab20-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="2ab20-107">Реализацией по умолчанию для процесса-суррогата является смешанный COM-сервер стиля модели.</span><span class="sxs-lookup"><span data-stu-id="2ab20-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="2ab20-108">При загрузке нескольких серверов DLL в один процесс-суррогат этот процесс обеспечивает создание экземпляров каждого сервера DLL с помощью потоковой модели, указанной в реестре для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="2ab20-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="2ab20-109">Все загруженные свободные потоковые серверы будут объединены в многопоточное подразделение, а каждый попотоковый сервер будет находиться в однопотоковом подразделении.</span><span class="sxs-lookup"><span data-stu-id="2ab20-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="2ab20-110">Если сервер DLL поддерживает обе модели потоков, COM выберет многопоточность.</span><span class="sxs-lookup"><span data-stu-id="2ab20-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="2ab20-111">Этот суррогатный процесс написан таким образом, что COM обрабатывает как выгрузку серверов DLL, так и завершение процесса-суррогата.</span><span class="sxs-lookup"><span data-stu-id="2ab20-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="2ab20-112">Предоставляемый системой суррогат будет прекрасно работать для большинства разработчиков, а также очень удобен в использовании.</span><span class="sxs-lookup"><span data-stu-id="2ab20-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="2ab20-113">Однако разработчики с особыми соображениями могут решить, что необходим пользовательский суррогат.</span><span class="sxs-lookup"><span data-stu-id="2ab20-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="2ab20-114">Дополнительные сведения см. [в разделе Написание пользовательского суррогата](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="2ab20-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ab20-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2ab20-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ab20-116">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="2ab20-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




