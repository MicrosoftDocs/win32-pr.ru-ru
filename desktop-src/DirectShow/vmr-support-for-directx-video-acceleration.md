---
description: Поддержка VMR для ускорения видео DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Поддержка VMR для ускорения видео DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696734"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Поддержка VMR для ускорения видео DirectX

Ускорение видео DirectX — это интерфейс прикладного программирования (API) и соответствующий интерфейс драйвера устройства (DDI) для аппаратного ускорения обработки декодирования цифрового видео с поддержкой альфа-смешения для таких целей, как поддержка подизображений DVD. DirectX ва описан в Windows DDK. В этом пакете SDK описан интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , который обеспечивает доступ к функциональности DirectX в пользовательском режиме на аппаратном устройстве.

VMR поддерживает [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), и его реализация идентична старому наложению Mixer за исключением одного важного отличия. наложение Mixer гарантирует, что выходные данные подготавливаются к просмотру в области наложения, тогда как VMR может отправить выходные данные для дальнейшей обработки, например трехмерную операцию, или отправить выходные данные на поверхность, которая затем блиттед на основную поверхность.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Об ускорении видео DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



