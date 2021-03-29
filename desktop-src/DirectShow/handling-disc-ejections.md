---
description: Обработка извлечения с диска
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Обработка извлечения с диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894053"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="2dded-103">Обработка извлечения с диска</span><span class="sxs-lookup"><span data-stu-id="2dded-103">Handling Disc Ejections</span></span>

<span data-ttu-id="2dded-104">Когда пользователь извлекает DVD-диск из дисковода, Навигатор DVD отправляет в приложение \_ сообщение, извлеченное с DVD- \_ диска EC \_ .</span><span class="sxs-lookup"><span data-stu-id="2dded-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="2dded-105">Приложение может спокойно проигнорировать это сообщение и позволить DVD-навигатору управлять состоянием графика.</span><span class="sxs-lookup"><span data-stu-id="2dded-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="2dded-106">Приложение также может \_ \_ использовать извлеченный с DVD-диска EC \_ метод для реализации пользовательского поведения при извлечении диска.</span><span class="sxs-lookup"><span data-stu-id="2dded-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="2dded-107">При обработке сообщения необходимо установить \_ для флага РЕСЕТОНСТОП DVD **значение true** с помощью метода [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , а затем вызвать [**имедиаконтрол:: остановитесь**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) перед закрытием приложения или воспроизведением другого диска.</span><span class="sxs-lookup"><span data-stu-id="2dded-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dded-108">См. также</span><span class="sxs-lookup"><span data-stu-id="2dded-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dded-109">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="2dded-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



