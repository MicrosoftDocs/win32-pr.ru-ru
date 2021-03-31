---
description: Содержит внешние камеры для потока.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Атрибут MFStreamExtension_CameraExtrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155363"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a><span data-ttu-id="57012-103">Мфстреамекстенсион \_ камераекстринсикс, атрибут</span><span class="sxs-lookup"><span data-stu-id="57012-103">MFStreamExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="57012-104">Содержит внешние камеры для потока.</span><span class="sxs-lookup"><span data-stu-id="57012-104">Contains the camera extrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="57012-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="57012-105">Data type</span></span>

<span data-ttu-id="57012-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="57012-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="57012-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="57012-107">Get/set</span></span>

<span data-ttu-id="57012-108">Чтобы получить этот атрибут, вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="57012-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="57012-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57012-109">Remarks</span></span>

<span data-ttu-id="57012-110">Значением атрибута является [**мфкамераекстринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="57012-110">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="57012-111">Требования</span><span class="sxs-lookup"><span data-stu-id="57012-111">Requirements</span></span>



| <span data-ttu-id="57012-112">Требование</span><span class="sxs-lookup"><span data-stu-id="57012-112">Requirement</span></span> | <span data-ttu-id="57012-113">Значение</span><span class="sxs-lookup"><span data-stu-id="57012-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57012-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57012-114">Minimum supported client</span></span><br/> | <span data-ttu-id="57012-115">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="57012-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57012-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57012-116">Minimum supported server</span></span><br/> | <span data-ttu-id="57012-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="57012-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="57012-118">Header</span><span class="sxs-lookup"><span data-stu-id="57012-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="57012-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="57012-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




