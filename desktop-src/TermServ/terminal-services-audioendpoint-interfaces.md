---
title: Интерфейсы службы удаленных рабочих столов Аудиоендпоинт
description: С API Аудиоендпоинт используются следующие интерфейсы.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681414"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="1d6e7-103">Интерфейсы службы удаленных рабочих столов Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="1d6e7-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="1d6e7-104">С API Аудиоендпоинт используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1d6e7-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1d6e7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="1d6e7-106">**иаудиодевицеендпоинт**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="1d6e7-107">Инициализирует объект конечной точки устройства и получает возможности устройства, которое оно представляет.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="1d6e7-108">**иаудиоендпоинт**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="1d6e7-109">Предоставляет сведения для обработчика аудио о конечной точке аудио.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="1d6e7-110">Этот интерфейс реализуется конечной точкой аудио.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="1d6e7-111">**иаудиоендпоинтконтрол**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="1d6e7-112">Управляет состоянием потока конечной точки.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="1d6e7-113">**иаудиоендпоинтрт**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="1d6e7-114">Возвращает разницу между текущими позициями чтения и записи в буфере конечной точки.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="1d6e7-115">**иаудиоинпутендпоинтрт**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="1d6e7-116">Возвращает входной буфер для каждого прохода обработки.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="1d6e7-117">**иаудиуутпутендпоинтрт**</span><span class="sxs-lookup"><span data-stu-id="1d6e7-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="1d6e7-118">Возвращает выходной буфер для каждого прохода обработки.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d6e7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d6e7-119">Remarks</span></span>

<span data-ttu-id="1d6e7-120">Службы удаленных рабочих столов API Аудиоендпоинт для использования в сценариях удаленный рабочий стол; Он не предназначен для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="1d6e7-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




