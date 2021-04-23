---
title: Справочник по API службы удаленных рабочих столов Аудиоендпоинт
description: Поддерживает интерфейсы для регистрации конечных точек аудио и передачи данных.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Справочник по API Аудиоендпоинт службы удаленных рабочих столов службы удаленных рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411200"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="3e37a-104">Справочник по API службы удаленных рабочих столов Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="3e37a-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="3e37a-105">*Конечная точка аудио* представляет собой звуковое устройство, аудио API или любой другой источник или приемник звука, и используется для отправки данных в модуль аудио и получения данных из него.</span><span class="sxs-lookup"><span data-stu-id="3e37a-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="3e37a-106">Конечная точка аудио должна быть подключена к подсистеме аудио с помощью *подключения*, и к каждому подключению может быть подключена только одна конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3e37a-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="3e37a-107">После регистрации конечной точки обработчик звука присоединяет конечную точку к подключению.</span><span class="sxs-lookup"><span data-stu-id="3e37a-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="3e37a-108">Каждый объект конечной точки должен реализовывать следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="3e37a-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="3e37a-109">[**Иаудиоендпоинт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) , чтобы включить обработчику аудио для получения сведений о конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3e37a-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="3e37a-110">[**Иаудиоендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) получить сведения о буфере данных перед выполнением прохода обработки и уведомить конечную точку о завершении прохода.</span><span class="sxs-lookup"><span data-stu-id="3e37a-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="3e37a-111">Интерфейс [**иаудиоинпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) или [**иаудиуутпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) в зависимости от того, захватывается ли объект конечной точки или готовится к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3e37a-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="3e37a-112">**иаудиодевицеендпоинт**</span><span class="sxs-lookup"><span data-stu-id="3e37a-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="3e37a-113">**иаудиоендпоинтконтрол**</span><span class="sxs-lookup"><span data-stu-id="3e37a-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="3e37a-114">Обработчик аудио использует эти интерфейсы для получения сведений о конечных точках, подключенных к подсистеме.</span><span class="sxs-lookup"><span data-stu-id="3e37a-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="3e37a-115">Реализация конечной точки должна предоставлять механизм для доставки данных в подсистему или получения данных из него, как указано в этих интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="3e37a-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="3e37a-116">Службы удаленных рабочих столов API Аудиоендпоинт поддерживает типы перечисления, интерфейсы и структуры.</span><span class="sxs-lookup"><span data-stu-id="3e37a-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e37a-117">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="3e37a-117">In this section</span></span>

-   [<span data-ttu-id="3e37a-118">Типы перечисления службы удаленных рабочих столов Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="3e37a-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="3e37a-119">службы удаленных рабочих столов функции Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="3e37a-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="3e37a-120">Интерфейсы службы удаленных рабочих столов Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="3e37a-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="3e37a-121">службы удаленных рабочих столов структур Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="3e37a-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="3e37a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e37a-122">Remarks</span></span>

<span data-ttu-id="3e37a-123">Службы удаленных рабочих столов API Аудиоендпоинт для использования в сценариях удаленный рабочий стол; Он не предназначен для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="3e37a-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




