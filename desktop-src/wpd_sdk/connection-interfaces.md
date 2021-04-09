---
description: Интерфейсы подключения MTP и Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Интерфейсы подключения MTP и Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081443"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="9bfbe-103">Интерфейсы подключения MTP и Bluetooth</span><span class="sxs-lookup"><span data-stu-id="9bfbe-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="9bfbe-104">Следующие интерфейсы позволяют приложениям перечислять и подключаться только к устройствам, поддерживающим протокол передачи мультимедиа (MTP) через Bluetooth (MTP/Bluetooth).</span><span class="sxs-lookup"><span data-stu-id="9bfbe-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="9bfbe-105">Интерфейсы драйвера, коллекции и клиента WPD не ограничиваются протоколом MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="9bfbe-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="9bfbe-106">Interface</span></span>                                                              | <span data-ttu-id="9bfbe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9bfbe-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bfbe-108">**иконнектионрекуесткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9bfbe-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="9bfbe-109">Определяет один метод обратного вызова, используемый приложениями для получения уведомлений о завершенных и отмененных запросах.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="9bfbe-110">**иенумпортабледевицеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="9bfbe-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="9bfbe-111">Перечисляет интерфейсы **ипортабледевицеконнектор** .</span><span class="sxs-lookup"><span data-stu-id="9bfbe-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="9bfbe-112">**ипортабледевицеконнектор**</span><span class="sxs-lookup"><span data-stu-id="9bfbe-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="9bfbe-113">Поддерживает методы, которые вызываются приложениями для установки подключений к устройствам MTP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="9bfbe-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9bfbe-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bfbe-115">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="9bfbe-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



