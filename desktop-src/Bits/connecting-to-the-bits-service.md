---
title: Подключение к службе BITS
description: Чтобы подключиться к службе BITS, создайте экземпляр объекта Баккграундкопиманажер, как показано в следующем примере.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134095"
---
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="6cccd-103">Подключение к службе BITS</span><span class="sxs-lookup"><span data-stu-id="6cccd-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="6cccd-104">Чтобы подключиться к системной службе BITS, создайте экземпляр объекта Баккграундкопиманажер, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6cccd-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="6cccd-105">Системная служба BITS — это системная служба Windows, выполняемая на клиентском компьютере, в которой реализована возможность передачи в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6cccd-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



<span data-ttu-id="6cccd-106">Чтобы проверить наличие определенной версии BITS, используйте символьный идентификатор класса для Баккграундкопиманажер в зависимости от версии, которую необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="6cccd-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="6cccd-107">Например, чтобы проверить наличие BITS 10,2, используйте CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="6cccd-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="6cccd-108">В следующем примере показано, как использовать один из символьных идентификаторов классов.</span><span class="sxs-lookup"><span data-stu-id="6cccd-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



<span data-ttu-id="6cccd-109">Используйте методы интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) для [создания заданий перемещения](creating-a-job.md), [перечисления заданий](enumerating-jobs-in-the-transfer-queue.md) в очереди и [получения заданий](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="6cccd-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="6cccd-110">Служба BITS требует, чтобы прокси-серверы интерфейса клиента использовали олицетворение или уровень ОЛИЦЕТВОРЕНия.</span><span class="sxs-lookup"><span data-stu-id="6cccd-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="6cccd-111">Если приложение не вызывает [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com использует функцию Identify по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cccd-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="6cccd-112">Служба BITS завершается с ошибкой E \_ ACCESSDENIED, если не задан правильный уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="6cccd-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="6cccd-113">Если вы предоставляете библиотеку, которая выполняет интерфейсы BITS, и приложение, вызывающее библиотеку, задает уровень олицетворения, приведенный ниже, необходимо вызвать метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) , чтобы задать правильный уровень олицетворения для каждого вызываемого интерфейса BITS.</span><span class="sxs-lookup"><span data-stu-id="6cccd-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="6cccd-114">Перед завершением работы приложения Освободите копию указателя интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6cccd-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="6cccd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6cccd-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6cccd-116">[Вызов BITS из .NET и C#](/windows/desktop/Bits/bits-dot-net) для BITS</span><span class="sxs-lookup"><span data-stu-id="6cccd-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 