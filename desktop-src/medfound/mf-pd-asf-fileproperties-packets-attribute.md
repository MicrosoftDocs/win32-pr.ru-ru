---
description: Указывает число пакетов в разделе данных файла расширенных систем формата ASF.
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: Атрибут MF_PD_ASF_FILEPROPERTIES_PACKETS (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991088"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="77648-103">\_ \_ \_ Атрибут пакетов MF филепропертиес \_ ASF</span><span class="sxs-lookup"><span data-stu-id="77648-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="77648-104">Указывает число пакетов в разделе данных файла расширенных систем формата ASF.</span><span class="sxs-lookup"><span data-stu-id="77648-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="77648-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="77648-105">Data type</span></span>

<span data-ttu-id="77648-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="77648-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="77648-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77648-107">Remarks</span></span>

<span data-ttu-id="77648-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="77648-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="77648-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="77648-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="77648-110">Требования</span><span class="sxs-lookup"><span data-stu-id="77648-110">Requirements</span></span>



| <span data-ttu-id="77648-111">Требование</span><span class="sxs-lookup"><span data-stu-id="77648-111">Requirement</span></span> | <span data-ttu-id="77648-112">Значение</span><span class="sxs-lookup"><span data-stu-id="77648-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77648-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77648-113">Minimum supported client</span></span><br/> | <span data-ttu-id="77648-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77648-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="77648-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77648-115">Minimum supported server</span></span><br/> | <span data-ttu-id="77648-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77648-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="77648-117">Header</span><span class="sxs-lookup"><span data-stu-id="77648-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="77648-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="77648-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77648-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77648-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77648-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77648-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="77648-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="77648-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="77648-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="77648-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="77648-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="77648-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="77648-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="77648-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="77648-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="77648-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="77648-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="77648-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




