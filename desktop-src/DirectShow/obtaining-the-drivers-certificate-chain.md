---
description: Получение цепочки сертификатов драйверов
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Получение цепочки сертификатов драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894098"
---
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="5ee3f-103">Получение цепочки сертификатов драйверов</span><span class="sxs-lookup"><span data-stu-id="5ee3f-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="5ee3f-104">Чтобы использовать протокол сертифицированной защиты выхода (Копп), приложение сначала должно создать граф DirectShow, включающий фильтр рендеринга видео микширования (VMR-7 или VMR-9).</span><span class="sxs-lookup"><span data-stu-id="5ee3f-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="5ee3f-105">Старый фильтр модуля подготовки отчетов не поддерживает Копп.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="5ee3f-106">Перед вызовом любых методов Копп приложение должно создать граф воспроизведения видео и подключить декодер к входному ПИН-коду фильтра VMR.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="5ee3f-107">Воспроизвести видеофайл необязательно.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="5ee3f-108">После построения графа запросите VMR для интерфейса [**иамцертифиедаутпутпротектион**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) , а затем вызовите [**Иамцертифиедаутпутпротектион:: кэйексчанже**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="5ee3f-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="5ee3f-109">Этот метод возвращает 128-разрядное случайное число, введенное в виде GUID, а также указатель на массив байтов, содержащий цепочку сертификатов XML драйвера в формате UTF-8.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="5ee3f-110">В следующем коде показано, как получить цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-110">The following code shows how to get the certificate chain.</span></span>


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a><span data-ttu-id="5ee3f-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5ee3f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee3f-112">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="5ee3f-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



