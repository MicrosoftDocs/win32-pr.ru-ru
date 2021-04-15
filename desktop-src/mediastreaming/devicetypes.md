---
title: Перечисление Девицетипес
description: Описание типов устройств DLNA, поддерживаемых API потоковой передачи мультимедиа.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API потоковой передачи мультимедиа для перечисления Девицетипес
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714079"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="79b6d-104">Перечисление Девицетипес</span><span class="sxs-lookup"><span data-stu-id="79b6d-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="79b6d-105">Описание типов устройств DLNA, поддерживаемых API потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="79b6d-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b6d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79b6d-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="79b6d-107">Константы</span><span class="sxs-lookup"><span data-stu-id="79b6d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="79b6d-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="79b6d-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="79b6d-109">Неизвестный тип устройства.</span><span class="sxs-lookup"><span data-stu-id="79b6d-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="79b6d-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**дигиталмедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="79b6d-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="79b6d-111">Модуль подготовки цифрового мультимедиа DLNA (ДМР).</span><span class="sxs-lookup"><span data-stu-id="79b6d-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="79b6d-112">Значение эквивалентно типу устройства **urn: schemas-UPnP-org: Device: медиарендерер: 1**.</span><span class="sxs-lookup"><span data-stu-id="79b6d-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="79b6d-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**дигиталмедиасервер**</span><span class="sxs-lookup"><span data-stu-id="79b6d-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="79b6d-114">Сервер цифрового мультимедиа DLNA (DMS).</span><span class="sxs-lookup"><span data-stu-id="79b6d-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="79b6d-115">Значение эквивалентно типу устройства **urn: schemas-UPnP-org: Device: медиасервер: 1**.</span><span class="sxs-lookup"><span data-stu-id="79b6d-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="79b6d-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**дигиталмедиаплайер**</span><span class="sxs-lookup"><span data-stu-id="79b6d-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="79b6d-117">Проигрыватель DLNA Digital Media Player</span><span class="sxs-lookup"><span data-stu-id="79b6d-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79b6d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="79b6d-118">Requirements</span></span>



| <span data-ttu-id="79b6d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="79b6d-119">Requirement</span></span> | <span data-ttu-id="79b6d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="79b6d-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b6d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="79b6d-121">IDL</span></span><br/> | <dl> <span data-ttu-id="79b6d-122"><dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="79b6d-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





