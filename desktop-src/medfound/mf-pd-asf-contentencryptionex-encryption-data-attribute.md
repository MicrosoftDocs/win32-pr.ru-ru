---
description: Содержит данные шифрования для файла ASF. Этот атрибут соответствует объекту расширенного шифрования содержимого в заголовке ASF, определенном в спецификации ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Атрибут MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344562"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="aa7ba-104">\_ \_ \_ \_ Атрибут данных шифрования MF PD ASF контентенкриптионекс \_</span><span class="sxs-lookup"><span data-stu-id="aa7ba-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="aa7ba-105">Содержит данные шифрования для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="aa7ba-106">Этот атрибут соответствует объекту расширенного шифрования содержимого в заголовке ASF, определенном в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa7ba-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aa7ba-107">Data type</span></span>

<span data-ttu-id="aa7ba-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="aa7ba-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="aa7ba-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa7ba-109">Remarks</span></span>

<span data-ttu-id="aa7ba-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="aa7ba-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из заголовка объекта расширенного шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="aa7ba-112">Размер большого двоичного объекта равен полю размера данных.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="aa7ba-113">Массив байтов, содержащийся в большом двоичном объекте, совпадает с полем данных в расширенном наборе шифрования содержимого заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7ba-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aa7ba-114">Requirements</span></span>



| <span data-ttu-id="aa7ba-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aa7ba-115">Requirement</span></span> | <span data-ttu-id="aa7ba-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aa7ba-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7ba-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa7ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7ba-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa7ba-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa7ba-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa7ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7ba-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa7ba-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aa7ba-121">Header</span><span class="sxs-lookup"><span data-stu-id="aa7ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa7ba-122"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ba-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa7ba-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa7ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7ba-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa7ba-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa7ba-125">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="aa7ba-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="aa7ba-126">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="aa7ba-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="aa7ba-127">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="aa7ba-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="aa7ba-128">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="aa7ba-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa7ba-129">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="aa7ba-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="aa7ba-130">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="aa7ba-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




