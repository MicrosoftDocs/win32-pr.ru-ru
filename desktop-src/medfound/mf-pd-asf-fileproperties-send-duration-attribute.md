---
description: Указывает время в 100-наносекундных единицах, необходимое для отправки файла ASF. Время отправки пакетов — это время, когда пакет должен быть доставлен по сети. Это не время презентации пакета.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Атрибут MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712405"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="ce6bd-105">\_ \_ \_ \_ \_ Атрибут длительности отправки для MF PD ASF филепропертиес</span><span class="sxs-lookup"><span data-stu-id="ce6bd-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="ce6bd-106">Указывает время в 100-наносекундных единицах, необходимое для отправки файла ASF.</span><span class="sxs-lookup"><span data-stu-id="ce6bd-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="ce6bd-107">*Время отправки* пакета — это время, когда пакет должен быть доставлен по сети.</span><span class="sxs-lookup"><span data-stu-id="ce6bd-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="ce6bd-108">Это не время презентации пакета.</span><span class="sxs-lookup"><span data-stu-id="ce6bd-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce6bd-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce6bd-109">Data type</span></span>

<span data-ttu-id="ce6bd-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ce6bd-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6bd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce6bd-111">Remarks</span></span>

<span data-ttu-id="ce6bd-112">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="ce6bd-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ce6bd-113">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="ce6bd-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6bd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ce6bd-114">Requirements</span></span>



| <span data-ttu-id="ce6bd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ce6bd-115">Requirement</span></span> | <span data-ttu-id="ce6bd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ce6bd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6bd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce6bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6bd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce6bd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce6bd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce6bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6bd-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce6bd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce6bd-121">Header</span><span class="sxs-lookup"><span data-stu-id="ce6bd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6bd-122"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6bd-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6bd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce6bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6bd-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce6bd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce6bd-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce6bd-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ce6bd-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ce6bd-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ce6bd-127">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="ce6bd-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ce6bd-128">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="ce6bd-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce6bd-129">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="ce6bd-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="ce6bd-130">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="ce6bd-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




