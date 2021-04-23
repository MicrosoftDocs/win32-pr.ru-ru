---
description: Указывает профиль аудио и уровень расширенного потока аудио-кодирования (AAC).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Атрибут MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718120"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="02957-103">\_ \_ \_ \_ \_ Атрибут индикации уровня профиля аудиоподсистемы \_ MF MT AAC</span><span class="sxs-lookup"><span data-stu-id="02957-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="02957-104">Указывает профиль аудио и уровень расширенного потока аудио-кодирования (AAC).</span><span class="sxs-lookup"><span data-stu-id="02957-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="02957-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="02957-105">Data type</span></span>

<span data-ttu-id="02957-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="02957-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="02957-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="02957-107">Get/set</span></span>

<span data-ttu-id="02957-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="02957-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="02957-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="02957-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="02957-110">Применение</span><span class="sxs-lookup"><span data-stu-id="02957-110">Applies To</span></span>

[<span data-ttu-id="02957-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="02957-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="02957-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02957-112">Remarks</span></span>

<span data-ttu-id="02957-113">Этот атрибут содержит значение поля **аудиопрофилелевелиндикатион** , как определено в стандарте ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="02957-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="02957-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="02957-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="02957-115">Требования</span><span class="sxs-lookup"><span data-stu-id="02957-115">Requirements</span></span>



| <span data-ttu-id="02957-116">Требование</span><span class="sxs-lookup"><span data-stu-id="02957-116">Requirement</span></span> | <span data-ttu-id="02957-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02957-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02957-118">Header</span><span class="sxs-lookup"><span data-stu-id="02957-118">Header</span></span><br/> | <dl> <span data-ttu-id="02957-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="02957-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02957-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02957-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02957-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02957-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02957-122">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="02957-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




