---
description: Указывает идентификатор файла в формате ASF.
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: Атрибут MF_PD_ASF_FILEPROPERTIES_FILE_ID (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656565"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="b66c5-103">\_ \_ \_ \_ Атрибут идентификатора файла филепропертиес MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="b66c5-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="b66c5-104">Указывает идентификатор файла в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="b66c5-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b66c5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b66c5-105">Data type</span></span>

<span data-ttu-id="b66c5-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b66c5-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b66c5-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b66c5-107">Remarks</span></span>

<span data-ttu-id="b66c5-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="b66c5-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b66c5-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="b66c5-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66c5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b66c5-110">Requirements</span></span>



| <span data-ttu-id="b66c5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b66c5-111">Requirement</span></span> | <span data-ttu-id="b66c5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b66c5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b66c5-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b66c5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b66c5-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b66c5-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b66c5-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b66c5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b66c5-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b66c5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b66c5-117">Header</span><span class="sxs-lookup"><span data-stu-id="b66c5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66c5-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b66c5-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b66c5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b66c5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66c5-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b66c5-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b66c5-121">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="b66c5-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b66c5-122">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="b66c5-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b66c5-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="b66c5-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b66c5-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="b66c5-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b66c5-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="b66c5-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b66c5-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="b66c5-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




