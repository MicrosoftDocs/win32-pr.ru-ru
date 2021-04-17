---
description: Указывает, использует ли файл в расширенном системном формате (ASF) кодирование с переменной скоростью (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: Атрибут MF_PD_ASF_METADATA_IS_VBR (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683874"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="b7ec7-103">MF \_ PD \_ \_ метаданные ASF \_ — \_ атрибут VBR</span><span class="sxs-lookup"><span data-stu-id="b7ec7-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="b7ec7-104">Указывает, использует ли файл в расширенном системном формате (ASF) кодирование с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="b7ec7-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7ec7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b7ec7-105">Data type</span></span>

<span data-ttu-id="b7ec7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b7ec7-106">**UINT32**</span></span>

<span data-ttu-id="b7ec7-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7ec7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7ec7-108">Remarks</span></span>

<span data-ttu-id="b7ec7-109">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="b7ec7-110">Если значение равно **true**, файл был закодирован с помощью VBR.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="b7ec7-111">Если значение равно **false** или отсутствует атрибут, файл не использует кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="b7ec7-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут и задает его в дескрипторе представления.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="b7ec7-113">Этот атрибут соответствует атрибуту **исвбр** в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7ec7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7ec7-114">Requirements</span></span>



| <span data-ttu-id="b7ec7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7ec7-115">Requirement</span></span> | <span data-ttu-id="b7ec7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7ec7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ec7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7ec7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ec7-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7ec7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7ec7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7ec7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ec7-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7ec7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7ec7-121">Header</span><span class="sxs-lookup"><span data-stu-id="b7ec7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7ec7-122"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ec7-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ec7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7ec7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ec7-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7ec7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7ec7-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="b7ec7-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b7ec7-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b7ec7-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b7ec7-127">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="b7ec7-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b7ec7-128">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="b7ec7-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7ec7-129">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="b7ec7-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b7ec7-130">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="b7ec7-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




