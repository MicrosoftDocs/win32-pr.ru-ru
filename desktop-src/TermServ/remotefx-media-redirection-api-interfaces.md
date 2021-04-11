---
title: Интерфейсы API перенаправления мультимедиа RemoteFX
description: API перенаправления мультимедиа RemoteFX поддерживает следующие интерфейсы.
ms.assetid: 9fb19c56-67a8-40f1-b6f1-8448eb83b38c
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed66bdeba9d554af4b9b42c74f4e4db95484f4c1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334291"
---
# <a name="remotefx-media-redirection-api-interfaces"></a><span data-ttu-id="f7c2f-103">Интерфейсы API перенаправления мультимедиа RemoteFX</span><span class="sxs-lookup"><span data-stu-id="f7c2f-103">RemoteFX Media Redirection API interfaces</span></span>

<span data-ttu-id="f7c2f-104">API перенаправления мультимедиа RemoteFX поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-104">The RemoteFX media redirection API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f7c2f-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f7c2f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f7c2f-106">**ивтсбитмапрендерер**</span><span class="sxs-lookup"><span data-stu-id="f7c2f-106">**IWTSBitmapRenderer**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer)
</dt> <dd>

<span data-ttu-id="f7c2f-107">Используется динамически подключаемым модулем виртуального канала для отображения растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-107">Used by a dynamic virtual channel plug-in to render bitmaps.</span></span>

</dd> <dt>

[<span data-ttu-id="f7c2f-108">**ивтсбитмапрендереркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f7c2f-108">**IWTSBitmapRendererCallback**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderercallback)
</dt> <dd>

<span data-ttu-id="f7c2f-109">Динамический подключаемый модуль виртуального канала реализует этот интерфейс, чтобы получать уведомления при изменении размера области отрисовки.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-109">A dynamic virtual channel plug-in implements this interface to be notified when the size of the rendering area changes.</span></span>

</dd> <dt>

[<span data-ttu-id="f7c2f-110">**ивтсбитмапрендерсервице**</span><span class="sxs-lookup"><span data-stu-id="f7c2f-110">**IWTSBitmapRenderService**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderservice)
</dt> <dd>

<span data-ttu-id="f7c2f-111">Эта служба используется для создания визуального сопоставления на клиенте, соответствующем сопоставленному окну на сервере.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-111">This service is used to create a visual mapping on the client corresponding to a mapped window on the server.</span></span>

</dd> <dt>

[<span data-ttu-id="f7c2f-112">**ивтсплугинсервицепровидер**</span><span class="sxs-lookup"><span data-stu-id="f7c2f-112">**IWTSPluginServiceProvider**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtspluginserviceprovider)
</dt> <dd>

<span data-ttu-id="f7c2f-113">Предоставляет способ для динамических подключаемых модулей виртуальных каналов для запроса различных удаленный рабочий стол клиентских служб.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-113">Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.</span></span>

</dd> </dl>

 

 




