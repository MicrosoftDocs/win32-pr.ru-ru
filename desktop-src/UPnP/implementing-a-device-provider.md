---
title: Реализация поставщика устройства
description: Чтобы реализовать поставщик устройства, создайте объект, который предоставляет интерфейс Иупнпдевицепровидер.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487025"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="64f49-103">Реализация поставщика устройства</span><span class="sxs-lookup"><span data-stu-id="64f49-103">Implementing a Device Provider</span></span>

<span data-ttu-id="64f49-104">Чтобы реализовать поставщик устройства, создайте объект, который предоставляет интерфейс [**иупнпдевицепровидер**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="64f49-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="64f49-105">Этот объект должен быть зарегистрирован на узле устройства с помощью метода [**иупнпрегистрар:: регистердевицепровидер**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="64f49-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="64f49-106">Этот метод принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="64f49-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="64f49-107">Имя поставщика, которое должно быть уникальным на компьютере.</span><span class="sxs-lookup"><span data-stu-id="64f49-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="64f49-108">Идентификатор ProgID класса, реализующего поставщик устройства.</span><span class="sxs-lookup"><span data-stu-id="64f49-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="64f49-109">Строка инициализации, которая передается поставщику устройства при запуске.</span><span class="sxs-lookup"><span data-stu-id="64f49-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="64f49-110">Идентификатор контейнера.</span><span class="sxs-lookup"><span data-stu-id="64f49-110">A container ID.</span></span> <span data-ttu-id="64f49-111">Идентификатор контейнера — это строка, идентифицирующая группу, к которой принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="64f49-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="64f49-112">Все устройства с одинаковым идентификатором контейнера размещаются в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="64f49-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




