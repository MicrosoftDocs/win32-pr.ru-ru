---
description: Указывает размер (в байтах) раздела данных в файле расширенного формата систем (ASF).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: Атрибут MF_PD_ASF_DATA_LENGTH (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656543"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="833d2-103">\_ \_ \_ Атрибут длины данных ASF для MF PD \_</span><span class="sxs-lookup"><span data-stu-id="833d2-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="833d2-104">Указывает размер (в байтах) раздела данных в файле расширенного формата систем (ASF).</span><span class="sxs-lookup"><span data-stu-id="833d2-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="833d2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="833d2-105">Data type</span></span>

<span data-ttu-id="833d2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="833d2-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="833d2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="833d2-107">Remarks</span></span>

<span data-ttu-id="833d2-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="833d2-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="833d2-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="833d2-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="833d2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="833d2-110">Requirements</span></span>



| <span data-ttu-id="833d2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="833d2-111">Requirement</span></span> | <span data-ttu-id="833d2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="833d2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="833d2-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="833d2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="833d2-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="833d2-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="833d2-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="833d2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="833d2-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="833d2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="833d2-117">Header</span><span class="sxs-lookup"><span data-stu-id="833d2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="833d2-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="833d2-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833d2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="833d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833d2-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="833d2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="833d2-121">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="833d2-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="833d2-122">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="833d2-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="833d2-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="833d2-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="833d2-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="833d2-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="833d2-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="833d2-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




