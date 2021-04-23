---
description: До 2006 августа WS-MetadataExchange определен собственный метод получения метаданных Get, который использовался профилем устройств для веб-служб (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Соответствие спецификации WS-MetadataExchange и WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155802"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="5a027-103">Соответствие спецификации WS-MetadataExchange и WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="5a027-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="5a027-104">До 2006 августа [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) определил собственный метод [получения метаданных Get](get--metadata-exchange--http-request-and-message.md) , который использовался [профилем устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="5a027-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="5a027-105">Спецификация WS-MetadataExchange версии 1,1 заменила этот метод методом GET, определенным в спецификации WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="5a027-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="5a027-106">В текущей модели WS-Transfer предоставляет метод [Get](get--metadata-exchange--http-request-and-message.md) и не делает ссылку на тип тела.</span><span class="sxs-lookup"><span data-stu-id="5a027-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="5a027-107">WS-MetadataExchange описывает формат текста и механизм упаковки нескольких фрагментов метаданных в одном ответе, а DPWS описывает конкретные фрагменты метаданных, которые служба должна включать в ответ на метаданные.</span><span class="sxs-lookup"><span data-stu-id="5a027-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="5a027-108">WSDAPI не полностью поддерживает спецификацию WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="5a027-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="5a027-109">Поскольку для устройств требуется только метод [Get](get--metadata-exchange--http-request-and-message.md) , никакие другие части WS-Transfer не реализованы.</span><span class="sxs-lookup"><span data-stu-id="5a027-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="5a027-110">Кроме того, WSDAPI не реализует дополнительный метод, описанный в WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="5a027-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



