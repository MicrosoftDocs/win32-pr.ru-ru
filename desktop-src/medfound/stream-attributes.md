---
description: Атрибуты потока
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Атрибуты потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543791"
---
# <a name="stream-attributes"></a><span data-ttu-id="8ed3a-103">Атрибуты потока</span><span class="sxs-lookup"><span data-stu-id="8ed3a-103">Stream Attributes</span></span>

<span data-ttu-id="8ed3a-104">Следующие атрибуты применяются к потокам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="8ed3a-105">Чтобы получить атрибуты из примера носителя, используйте метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="8ed3a-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="8ed3a-106">attribute</span><span class="sxs-lookup"><span data-stu-id="8ed3a-106">Attribute</span></span>                                                                                   | <span data-ttu-id="8ed3a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8ed3a-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="8ed3a-108">Мфстреамекстенсион \_ камераекстринсикс</span><span class="sxs-lookup"><span data-stu-id="8ed3a-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="8ed3a-109">Внешние камеры для потока.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="8ed3a-110">Мфстреамекстенсион \_ пинхолекамераинтринсикс</span><span class="sxs-lookup"><span data-stu-id="8ed3a-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="8ed3a-111">Встроенные функции камеры пинхоле для потока.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="8ed3a-112">Не каждый поток мультимедиа содержит все перечисленные здесь атрибуты.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="8ed3a-113">В некоторых случаях атрибут применяется только к определенным типам данных.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ed3a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8ed3a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ed3a-115">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="8ed3a-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="8ed3a-116">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ed3a-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ed3a-117">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="8ed3a-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



