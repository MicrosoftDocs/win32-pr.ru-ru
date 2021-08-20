---
title: Интерфейсы видео Direct3D
description: в этом разделе перечислены интерфейсы видео direct3d, доступные в direct3d 9Ex, которые поддерживаются в Windows 7 и более поздних версиях Windows клиентских операционных системах и в Windows server 2008 R2 и более поздних версиях Windows серверных операционных систем.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c59882c85a0c9feba1c011f81def65744a86b4fb04a9f43683eba7a3c1a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099142"
---
# <a name="direct3d-video-interfaces"></a>Интерфейсы видео Direct3D

в этом разделе перечислены интерфейсы видео direct3d, доступные в direct3d 9Ex, которые поддерживаются в Windows 7 и более поздних версиях Windows клиентских операционных системах и в Windows server 2008 R2 и более поздних версиях Windows серверных операционных систем. Вы можете использовать эти интерфейсы и их методы для получения возможностей защиты содержимого видео графического драйвера и аппаратных возможностей наложения устройства Direct3D. Вы также можете использовать эти интерфейсы и их методы для защиты видеосодержимого. Эти интерфейсы и их методы определены в D3d9. h и описаны в разделе [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .



| Интерфейс                                                                                                                                                                                                                             | Описание                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Запрашивает аппаратные возможности наложения устройства Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Предоставляет коммуникационный канал с графическим драйвером или средой выполнения Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Представляет сеанс шифрования, используемый для доступа к защищенной поверхности.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Позволяет приложению использовать службы защиты содержимого и шифрования, реализованные графическим драйвером.<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Руководство по программированию для Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

