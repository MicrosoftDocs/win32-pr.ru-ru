---
title: Параметры создания пула плиток
description: Параметры в этом разделе используются для определения пулов плиток с помощью API CreateBuffer ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067495"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="ebc55-103">Параметры создания пула плиток</span><span class="sxs-lookup"><span data-stu-id="ebc55-103">Tile pool creation parameters</span></span>

<span data-ttu-id="ebc55-104">Параметры в этом разделе используются для определения пулов плиток с помощью API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ebc55-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="ebc55-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Изменять**</span><span class="sxs-lookup"><span data-stu-id="ebc55-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ebc55-106">Размер выделения, кратный 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="ebc55-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="ebc55-107">0 является допустимым, так как позднее вы можете использовать операцию [**ID3D11DeviceContext2:: ресизетилепул**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .</span><span class="sxs-lookup"><span data-stu-id="ebc55-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="ebc55-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Поддерживаемые флаги для ресурсов**</span><span class="sxs-lookup"><span data-stu-id="ebc55-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ebc55-109">D3D11 \_ \_ \_ пул плиток ресурсов \_ (определяет ресурс как пул плиток), \_ \_ Общие ресурсы, общие \_ \_ \_ кэйедмутекс или \_ Общие \_ нсандле для ресурса D3D11.</span><span class="sxs-lookup"><span data-stu-id="ebc55-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="ebc55-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Поддерживаемое использование ресурсов**</span><span class="sxs-lookup"><span data-stu-id="ebc55-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="ebc55-111">D3D11 \_ использование \_ только по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebc55-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ebc55-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ebc55-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc55-113">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebc55-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




