---
description: WIA реализуется как сервер вне процесса COM, чтобы обеспечить надежную работу клиентских приложений.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Архитектура WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570475"
---
# <a name="wia-architecture"></a><span data-ttu-id="6e63c-103">Архитектура WIA</span><span class="sxs-lookup"><span data-stu-id="6e63c-103">WIA Architecture</span></span>

<span data-ttu-id="6e63c-104">WIA реализуется как сервер вне процесса COM, чтобы обеспечить надежную работу клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="6e63c-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="6e63c-105">В отличие от большинства приложений сервера обработки, получение изображений Windows (WIA) позволяет избежать снижения производительности во время пересылки данных образа, предоставляя собственный механизм обмена данными, [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="6e63c-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="6e63c-106">Этот высокопроизводительный интерфейс использует окно общей памяти для перемещения данных клиенту.</span><span class="sxs-lookup"><span data-stu-id="6e63c-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="6e63c-107">У WIA есть три основных компонента: диспетчер устройств, Библиотека службы Минидривер и Минидривер устройства.</span><span class="sxs-lookup"><span data-stu-id="6e63c-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="6e63c-108">Диспетчер устройств перечисляет устройства обработки изображений, получает свойства устройства, настраивает события для устройств и создает объекты устройств.</span><span class="sxs-lookup"><span data-stu-id="6e63c-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="6e63c-109">Библиотека служб Минидривер реализует все службы, независимые от устройства.</span><span class="sxs-lookup"><span data-stu-id="6e63c-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="6e63c-110">Устройство Минидривер сопоставляет свойства и команды WIA с конкретным устройством.</span><span class="sxs-lookup"><span data-stu-id="6e63c-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="6e63c-111">На следующей схеме показана архитектура WIA:</span><span class="sxs-lookup"><span data-stu-id="6e63c-111">The following diagram illustrates the WIA architecture:</span></span>

![Архитектура WIA](images/wiarch.gif)

 

 



