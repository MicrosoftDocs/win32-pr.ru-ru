---
description: Операционная система Microsoft Windows обеспечивает поддержку различных аппаратных устройств и сетевых протоколов, использующих архитектуру поставщика времени.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Поставщик времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911999"
---
# <a name="time-provider"></a><span data-ttu-id="6bf24-103">Поставщик времени</span><span class="sxs-lookup"><span data-stu-id="6bf24-103">Time Provider</span></span>

<span data-ttu-id="6bf24-104">Операционная система Microsoft Windows обеспечивает поддержку различных аппаратных устройств и сетевых протоколов, использующих архитектуру *поставщика времени* .</span><span class="sxs-lookup"><span data-stu-id="6bf24-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="6bf24-105">Поставщики входного времени получают точные отметки времени от оборудования или сети, а поставщики времени вывода предоставляют метки времени другим клиентам в сети.</span><span class="sxs-lookup"><span data-stu-id="6bf24-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="6bf24-106">Поставщики времени управляются *диспетчером поставщиков времени*.</span><span class="sxs-lookup"><span data-stu-id="6bf24-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="6bf24-107">Он отвечает за загрузку, запуск и остановку поставщиков времени, направляемых диспетчером управления службами.</span><span class="sxs-lookup"><span data-stu-id="6bf24-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="6bf24-108">Этот интерфейс упрощает написание поставщика времени, чем запись полной службы.</span><span class="sxs-lookup"><span data-stu-id="6bf24-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="6bf24-109">Создание поставщика времени</span><span class="sxs-lookup"><span data-stu-id="6bf24-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="6bf24-110">Регистрация поставщика времени</span><span class="sxs-lookup"><span data-stu-id="6bf24-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="6bf24-111">Пример поставщика времени</span><span class="sxs-lookup"><span data-stu-id="6bf24-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="6bf24-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6bf24-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf24-113">Служба времени Windows</span><span class="sxs-lookup"><span data-stu-id="6bf24-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



