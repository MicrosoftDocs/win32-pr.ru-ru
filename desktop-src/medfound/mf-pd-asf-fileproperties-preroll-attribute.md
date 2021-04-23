---
description: Указывает время в миллисекундах, в течение которого данные задаются в буфер перед воспроизведением файла ASF.
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: Атрибут MF_PD_ASF_FILEPROPERTIES_PREROLL (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265508"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="f569e-103">\_ \_ \_ Атрибут onрулона MF PD ASF филепропертиес \_</span><span class="sxs-lookup"><span data-stu-id="f569e-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="f569e-104">Указывает время в миллисекундах, в течение которого данные задаются в буфер перед воспроизведением файла ASF.</span><span class="sxs-lookup"><span data-stu-id="f569e-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f569e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f569e-105">Data type</span></span>

<span data-ttu-id="f569e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f569e-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="f569e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f569e-107">Remarks</span></span>

<span data-ttu-id="f569e-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="f569e-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f569e-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="f569e-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="f569e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f569e-110">Requirements</span></span>



| <span data-ttu-id="f569e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f569e-111">Requirement</span></span> | <span data-ttu-id="f569e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f569e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f569e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f569e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f569e-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f569e-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f569e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f569e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f569e-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f569e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f569e-117">Header</span><span class="sxs-lookup"><span data-stu-id="f569e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f569e-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="f569e-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f569e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f569e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f569e-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f569e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f569e-121">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="f569e-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f569e-122">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f569e-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="f569e-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="f569e-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f569e-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="f569e-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f569e-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="f569e-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f569e-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="f569e-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




