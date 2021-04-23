---
description: Объекты потоковой передачи мультимедиа
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Объекты потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351685"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="c8077-103">Объекты потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c8077-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="c8077-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="c8077-104">This API is deprecated.</span></span> <span data-ttu-id="c8077-105">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="c8077-105">New applications should not use it.</span></span>

 

<span data-ttu-id="c8077-106">В следующей таблице описаны объекты потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8077-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8077-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="c8077-107">CLSID</span></span></th>
<th><span data-ttu-id="c8077-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c8077-108">Description</span></span></th>
<th><span data-ttu-id="c8077-109">Поддерживаемые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="c8077-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8077-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="c8077-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="c8077-111">Может создавать примеры носителей для любого типа данных, поддерживаемого DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8077-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="c8077-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8077-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="c8077-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="c8077-117">Реализация объекта <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a> Audio Container.</span><span class="sxs-lookup"><span data-stu-id="c8077-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8077-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="c8077-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="c8077-120">Поток мультимедиа DirectDraw, который можно добавить в поток мультимедиа DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c8077-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>идиректдравмедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="c8077-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8077-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="c8077-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="c8077-127">Реализация DirectShow потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8077-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="c8077-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>имултимедиастреам</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8077-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="c8077-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="c8077-131">Предоставляет функции потоковой передачи мультимедиа для объекта CLSID_AMMultiMediaStream через интерфейс <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c8077-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8077-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c8077-133">N/A</span></span></td>
<td><span data-ttu-id="c8077-134">Примеры, созданные объектом CLSID_AMMediaTypeStream.</span><span class="sxs-lookup"><span data-stu-id="c8077-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="c8077-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="c8077-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8077-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c8077-138">N/A</span></span></td>
<td><span data-ttu-id="c8077-139">Примеры, созданные потоком DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c8077-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8077-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="c8077-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>идиректдравстреамсампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="c8077-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8077-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



