---
description: Указывает время, необходимое для воспроизведения ASF-файла (в единицах с 100 нс).
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Атрибут MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998953"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="a2c42-103">\_ \_ \_ \_ \_ Атрибут длительности воспроизведения для MF PD ASF филепропертиес</span><span class="sxs-lookup"><span data-stu-id="a2c42-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="a2c42-104">Указывает время, необходимое для воспроизведения ASF-файла (в единицах с 100 нс).</span><span class="sxs-lookup"><span data-stu-id="a2c42-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="a2c42-105">Это значение включает в себя время предвремени.</span><span class="sxs-lookup"><span data-stu-id="a2c42-105">This value includes the preroll time.</span></span> <span data-ttu-id="a2c42-106">Чтобы получить фактическое время воспроизведения, получите значение атрибута « [**Продолжительность MF \_ PD \_**](mf-pd-duration-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="a2c42-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="a2c42-107">Тем не менее, если предустановленное значение больше, чем длительность воспроизведения, значение **MF \_ PD \_ Duration** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a2c42-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2c42-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a2c42-108">Data type</span></span>

<span data-ttu-id="a2c42-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a2c42-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c42-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2c42-110">Remarks</span></span>

<span data-ttu-id="a2c42-111">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="a2c42-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a2c42-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="a2c42-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="a2c42-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2c42-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="a2c42-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2c42-114">Requirements</span></span>



| <span data-ttu-id="a2c42-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2c42-115">Requirement</span></span> | <span data-ttu-id="a2c42-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c42-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c42-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2c42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c42-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2c42-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2c42-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2c42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c42-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2c42-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2c42-121">Header</span><span class="sxs-lookup"><span data-stu-id="a2c42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2c42-122"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2c42-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c42-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2c42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c42-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2c42-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2c42-125">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="a2c42-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a2c42-126">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="a2c42-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a2c42-127">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="a2c42-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a2c42-128">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="a2c42-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2c42-129">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="a2c42-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a2c42-130">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="a2c42-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




