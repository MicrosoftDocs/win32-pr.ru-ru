---
description: Указывает минимальный размер пакета (в байтах) для файла в формате ASF.
ms.assetid: 8c62db36-1332-4565-9fc0-885b9fc148e1
title: Атрибут MF_PD_ASF_FILEPROPERTIES_MIN_PACKET_SIZE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e7b9016184096696ffd74cde6bd51f305778e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656566"
---
# <a name="mf_pd_asf_fileproperties_min_packet_size-attribute"></a><span data-ttu-id="cc542-103">\_ \_ \_ Атрибут филепропертиес мин, \_ \_ Размер пакета \_ для MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="cc542-103">MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="cc542-104">Указывает минимальный размер пакета (в байтах) для файла в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="cc542-104">Specifies the minimum packet size, in bytes, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="cc542-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc542-105">Data type</span></span>

<span data-ttu-id="cc542-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cc542-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cc542-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc542-107">Remarks</span></span>

<span data-ttu-id="cc542-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="cc542-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="cc542-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="cc542-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc542-110">Требования</span><span class="sxs-lookup"><span data-stu-id="cc542-110">Requirements</span></span>



| <span data-ttu-id="cc542-111">Требование</span><span class="sxs-lookup"><span data-stu-id="cc542-111">Requirement</span></span> | <span data-ttu-id="cc542-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cc542-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc542-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc542-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cc542-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc542-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc542-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc542-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cc542-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc542-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cc542-117">Header</span><span class="sxs-lookup"><span data-stu-id="cc542-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc542-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc542-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc542-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc542-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc542-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc542-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc542-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="cc542-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cc542-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cc542-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cc542-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="cc542-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="cc542-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="cc542-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc542-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="cc542-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="cc542-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="cc542-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




