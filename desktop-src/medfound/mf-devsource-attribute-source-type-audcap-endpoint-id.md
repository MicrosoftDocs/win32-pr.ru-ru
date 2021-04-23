---
description: Указывает идентификатор конечной точки для устройства записи звука.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694747"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="4920a-103">\_ \_ Тип источника атрибута MF девсаурце \_ \_ \_ \_ атрибут идентификатора конечной точки аудкап \_</span><span class="sxs-lookup"><span data-stu-id="4920a-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="4920a-104">Указывает идентификатор конечной точки для устройства записи звука.</span><span class="sxs-lookup"><span data-stu-id="4920a-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="4920a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4920a-105">Data type</span></span>

<span data-ttu-id="4920a-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="4920a-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="4920a-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4920a-107">Get/set</span></span>

<span data-ttu-id="4920a-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="4920a-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="4920a-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="4920a-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="4920a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4920a-110">Remarks</span></span>

<span data-ttu-id="4920a-111">Значением атрибута является идентификатор конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4920a-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="4920a-112">Этот атрибут используется со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="4920a-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="4920a-113">Его можно использовать в качестве входных данных для функций [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) и [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="4920a-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="4920a-114">В этом контексте атрибут указывает устройство аудиозаписи для функции.</span><span class="sxs-lookup"><span data-stu-id="4920a-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="4920a-115">Идентификатор конечной точки для данного устройства можно получить, вызвав метод [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) .</span><span class="sxs-lookup"><span data-stu-id="4920a-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="4920a-116">Дополнительные сведения см. в документации по API аудио.</span><span class="sxs-lookup"><span data-stu-id="4920a-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="4920a-117">Когда функция [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) перечисляет звуковые устройства, возвращаемые объекты активации содержат этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="4920a-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="4920a-118">Атрибут используется внутренне объектом активации при создании источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4920a-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="4920a-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4920a-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4920a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4920a-120">Requirements</span></span>



| <span data-ttu-id="4920a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4920a-121">Requirement</span></span> | <span data-ttu-id="4920a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4920a-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4920a-123">Header</span><span class="sxs-lookup"><span data-stu-id="4920a-123">Header</span></span><br/> | <dl> <span data-ttu-id="4920a-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4920a-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4920a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4920a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4920a-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4920a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4920a-127">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="4920a-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="4920a-128">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="4920a-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
