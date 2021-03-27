---
title: Интерфейсы видео Direct3D
description: В этом разделе перечислены интерфейсы видео Direct3D, доступные в Direct3D 9Ex и поддерживаемые в Windows 7 и более поздних версиях клиентских операционных систем Windows, а также в Windows Server 2008 R2 и более поздних версиях операционных систем Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487829"
---
# <a name="direct3d-video-interfaces"></a>Интерфейсы видео Direct3D

В этом разделе перечислены интерфейсы видео Direct3D, доступные в Direct3D 9Ex и поддерживаемые в Windows 7 и более поздних версиях клиентских операционных систем Windows, а также в Windows Server 2008 R2 и более поздних версиях операционных систем Windows Server. Вы можете использовать эти интерфейсы и их методы для получения возможностей защиты содержимого видео графического драйвера и аппаратных возможностей наложения устройства Direct3D. Вы также можете использовать эти интерфейсы и их методы для защиты видеосодержимого. Эти интерфейсы и их методы определены в D3d9. h и описаны в разделе [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .



| Интерфейс                                                                                                                                                                                                                             | Описание                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Запрашивает аппаратные возможности наложения устройства Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Предоставляет коммуникационный канал с графическим драйвером или средой выполнения Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Представляет сеанс шифрования, используемый для доступа к защищенной поверхности.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Позволяет приложению использовать службы защиты содержимого и шифрования, реализованные графическим драйвером.<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Руководство по программированию для Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

