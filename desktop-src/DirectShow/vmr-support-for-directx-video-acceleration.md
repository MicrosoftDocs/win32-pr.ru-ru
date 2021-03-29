---
description: Поддержка VMR для ускорения видео DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Поддержка VMR для ускорения видео DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811507"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Поддержка VMR для ускорения видео DirectX

Ускорение видео DirectX — это интерфейс прикладного программирования (API) и соответствующий интерфейс драйвера устройства (DDI) для аппаратного ускорения обработки декодирования цифрового видео с поддержкой альфа-смешения для таких целей, как поддержка подизображений DVD. DirectX ва описан в Windows DDK. В этом пакете SDK описан интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , который обеспечивает доступ к функциональности DirectX в пользовательском режиме на аппаратном устройстве.

VMR поддерживает [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), и его реализация идентична старому микшеру наложения, за исключением одного важного отличия. Микшер наложения гарантирует, что выходные данные будут отображены в область наложения, тогда как VMR может отправить выходные данные для дальнейшей обработки, например трехмерную операцию, или отправить выходные данные на поверхность, которая затем блиттед на основную поверхность.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Об ускорении видео DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



