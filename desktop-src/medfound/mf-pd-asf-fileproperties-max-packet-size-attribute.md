---
description: Указывает максимальный размер пакета (в байтах) для файла в формате ASF.
ms.assetid: 8dcae150-2363-47ba-b0d3-0bc182574d81
title: Атрибут MF_PD_ASF_FILEPROPERTIES_MAX_PACKET_SIZE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9c95b7511525570a9e04a33db8128f374f9472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656643"
---
# <a name="mf_pd_asf_fileproperties_max_packet_size-attribute"></a><span data-ttu-id="2dcaf-103">\_ \_ \_ \_ \_ \_ Атрибут максимального размера пакета MF PD ASF филепропертиес</span><span class="sxs-lookup"><span data-stu-id="2dcaf-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="2dcaf-104">Указывает максимальный размер пакета (в байтах) для файла в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="2dcaf-104">Specifies the maximum packet size, in bytes, of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2dcaf-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2dcaf-105">Data type</span></span>

<span data-ttu-id="2dcaf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2dcaf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2dcaf-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dcaf-107">Remarks</span></span>

<span data-ttu-id="2dcaf-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="2dcaf-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2dcaf-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="2dcaf-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dcaf-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2dcaf-110">Requirements</span></span>



| <span data-ttu-id="2dcaf-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2dcaf-111">Requirement</span></span> | <span data-ttu-id="2dcaf-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2dcaf-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dcaf-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dcaf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2dcaf-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dcaf-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2dcaf-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dcaf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2dcaf-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2dcaf-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2dcaf-117">Header</span><span class="sxs-lookup"><span data-stu-id="2dcaf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dcaf-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dcaf-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dcaf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dcaf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dcaf-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2dcaf-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dcaf-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="2dcaf-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2dcaf-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2dcaf-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2dcaf-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="2dcaf-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2dcaf-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="2dcaf-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dcaf-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="2dcaf-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2dcaf-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="2dcaf-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




