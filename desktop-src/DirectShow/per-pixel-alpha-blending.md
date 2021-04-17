---
description: Per-Pixel альфа-смешение
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel альфа-смешение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682245"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel альфа-смешение

Для многопиксельного альфа-смешения определены четыре подтипа носителей. Эти подтипы поддерживаются, только если VMR находится в режиме смешения. VMR отклоняет соединение, если он не находится в режиме смешения, когда вышестоящий фильтр пытается подключиться с помощью одного из этих подтипов. Эти подтипы определены в UUID. h:

-   МЕДИАСУБТИПЕ \_ ARGB1555
-   МЕДИАСУБТИПЕ \_ ARGB4444
-   МЕДИАСУБТИПЕ \_ ARGB32
-   МЕДИАСУБТИПЕ \_ айув

Дополнительные сведения см. в разделе [несжатые видео подтипы RGB](uncompressed-rgb-video-subtypes.md) и [**подтипы видеороликов YUV**](yuv-video-subtypes.md).

 

 



