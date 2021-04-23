---
description: Указывает число от 0 до 100, которое указывает на компромисс между качеством кодирования и скоростью кодирования.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Атрибут MF_TRANSCODE_QUALITYVSSPEED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708429"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="a55a1-103">\_Атрибут куалитивсспид для ПЕРЕКОДИРОВАНИЯ MF \_</span><span class="sxs-lookup"><span data-stu-id="a55a1-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="a55a1-104">Указывает число от 0 до 100, которое указывает на компромисс между качеством кодирования и скоростью кодирования.</span><span class="sxs-lookup"><span data-stu-id="a55a1-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="a55a1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a55a1-105">Data type</span></span>

<span data-ttu-id="a55a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a55a1-106">**UINT32**</span></span>

<span data-ttu-id="a55a1-107">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="a55a1-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="a55a1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a55a1-108">Value</span></span>                                                                          | <span data-ttu-id="a55a1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a55a1-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="a55a1-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a55a1-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="a55a1-111">Более низкое качество, более быстрая кодировка.</span><span class="sxs-lookup"><span data-stu-id="a55a1-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="a55a1-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="a55a1-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="a55a1-113">Более высокое качество, медленная кодировка.</span><span class="sxs-lookup"><span data-stu-id="a55a1-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="a55a1-114">Get/Set</span><span class="sxs-lookup"><span data-stu-id="a55a1-114">Get/set</span></span>

<span data-ttu-id="a55a1-115">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a55a1-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a55a1-116">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a55a1-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a55a1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a55a1-117">Remarks</span></span>

<span data-ttu-id="a55a1-118">Этот атрибут имеет то же значение GUID, что и свойство [авенккоммонкуалитивсспид](../directshow/avenccommonqualityvsspeed-property.md) , определенное для [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi), и имеет такую же интерпретацию.</span><span class="sxs-lookup"><span data-stu-id="a55a1-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="a55a1-119">Приложение может задать этот атрибут в профиле перекодировки перед созданием топологии для кодирования кодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a55a1-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="a55a1-120">Значение должно находиться в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="a55a1-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="a55a1-121">Для видеопотока построитель топологии перекодировки сопоставляет значение с заданным приложением значением и предоставляет сопоставленное значение свойству **мфпкэй \_ комплекситекс** кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a55a1-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="a55a1-122">Более низкие значения позволяют кодировщику использовать менее сложные алгоритмы кодирования.</span><span class="sxs-lookup"><span data-stu-id="a55a1-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="a55a1-123">Использование более простых алгоритмов обеспечивает более низкое качество вывода, но процесс кодирования выполняется быстрее и требует меньше вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="a55a1-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="a55a1-124">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a55a1-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a55a1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a55a1-125">Requirements</span></span>



| <span data-ttu-id="a55a1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a55a1-126">Requirement</span></span> | <span data-ttu-id="a55a1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a55a1-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a55a1-128">Header</span><span class="sxs-lookup"><span data-stu-id="a55a1-128">Header</span></span><br/> | <dl> <span data-ttu-id="a55a1-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a55a1-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a55a1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a55a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a55a1-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a55a1-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a55a1-132">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="a55a1-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="a55a1-133">**Имфтранскодепрофиле:: Сетвидеоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="a55a1-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
