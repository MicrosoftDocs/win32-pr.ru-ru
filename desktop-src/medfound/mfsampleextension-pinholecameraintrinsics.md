---
description: Содержит встроенные функции камеры пинхоле для образца.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Атрибут MFSampleExtension_PinholeCameraIntrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719469"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="a6d4c-103">Мфсампликстенсион \_ пинхолекамераинтринсикс, атрибут</span><span class="sxs-lookup"><span data-stu-id="a6d4c-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="a6d4c-104">Содержит встроенные функции камеры пинхоле для образца.</span><span class="sxs-lookup"><span data-stu-id="a6d4c-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6d4c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a6d4c-105">Data type</span></span>

<span data-ttu-id="a6d4c-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="a6d4c-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="a6d4c-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="a6d4c-107">Get/set</span></span>

<span data-ttu-id="a6d4c-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="a6d4c-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="a6d4c-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="a6d4c-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a6d4c-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="a6d4c-110">Applies to</span></span>

[<span data-ttu-id="a6d4c-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="a6d4c-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="a6d4c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6d4c-112">Remarks</span></span>

<span data-ttu-id="a6d4c-113">Значением атрибута является [**мфпинхолекамераинтринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="a6d4c-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="a6d4c-114">Этот атрибут является необязательным для поддержки камер, которые не были откалиброваны.</span><span class="sxs-lookup"><span data-stu-id="a6d4c-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d4c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a6d4c-115">Requirements</span></span>



| <span data-ttu-id="a6d4c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a6d4c-116">Requirement</span></span> | <span data-ttu-id="a6d4c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a6d4c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d4c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6d4c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d4c-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a6d4c-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6d4c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6d4c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d4c-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6d4c-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a6d4c-122">Header</span><span class="sxs-lookup"><span data-stu-id="a6d4c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6d4c-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d4c-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




