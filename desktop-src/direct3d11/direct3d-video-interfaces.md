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
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="ed520-103">Интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="ed520-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="ed520-104">В этом разделе перечислены интерфейсы видео Direct3D, доступные в Direct3D 9Ex и поддерживаемые в Windows 7 и более поздних версиях клиентских операционных систем Windows, а также в Windows Server 2008 R2 и более поздних версиях операционных систем Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ed520-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="ed520-105">Вы можете использовать эти интерфейсы и их методы для получения возможностей защиты содержимого видео графического драйвера и аппаратных возможностей наложения устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ed520-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="ed520-106">Вы также можете использовать эти интерфейсы и их методы для защиты видеосодержимого.</span><span class="sxs-lookup"><span data-stu-id="ed520-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="ed520-107">Эти интерфейсы и их методы определены в D3d9. h и описаны в разделе [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .</span><span class="sxs-lookup"><span data-stu-id="ed520-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="ed520-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ed520-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="ed520-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ed520-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed520-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="ed520-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="ed520-111">Запрашивает аппаратные возможности наложения устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ed520-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="ed520-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="ed520-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="ed520-113">Предоставляет коммуникационный канал с графическим драйвером или средой выполнения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ed520-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="ed520-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="ed520-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="ed520-115">Представляет сеанс шифрования, используемый для доступа к защищенной поверхности.</span><span class="sxs-lookup"><span data-stu-id="ed520-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="ed520-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="ed520-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="ed520-117">Позволяет приложению использовать службы защиты содержимого и шифрования, реализованные графическим драйвером.</span><span class="sxs-lookup"><span data-stu-id="ed520-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ed520-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ed520-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed520-119">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ed520-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="ed520-120">Руководство по программированию для Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ed520-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

