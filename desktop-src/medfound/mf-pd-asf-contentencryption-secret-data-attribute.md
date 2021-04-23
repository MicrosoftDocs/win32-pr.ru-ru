---
description: Содержит секретные данные для зашифрованного файла расширенных систем (ASF). Этот атрибут соответствует полю данных секрета в заголовке шифрования содержимого, определенном в спецификации ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Атрибут MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541359"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="4b233-104">\_ \_ \_ \_ Атрибут данных секрета MF PD ASF контентенкриптион \_</span><span class="sxs-lookup"><span data-stu-id="4b233-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="4b233-105">Содержит секретные данные для зашифрованного файла расширенных систем (ASF).</span><span class="sxs-lookup"><span data-stu-id="4b233-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="4b233-106">Этот атрибут соответствует полю данных секрета в заголовке шифрования содержимого, определенном в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="4b233-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b233-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4b233-107">Data type</span></span>

<span data-ttu-id="4b233-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="4b233-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="4b233-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b233-109">Remarks</span></span>

<span data-ttu-id="4b233-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="4b233-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="4b233-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) заполняет массив байтов полем секретных данных.</span><span class="sxs-lookup"><span data-stu-id="4b233-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="4b233-112">Размер массива равен значению поля "Секретная длина данных" заголовка шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="4b233-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b233-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4b233-113">Requirements</span></span>



| <span data-ttu-id="4b233-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4b233-114">Requirement</span></span> | <span data-ttu-id="4b233-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4b233-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b233-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b233-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4b233-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b233-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4b233-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b233-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4b233-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b233-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b233-120">Header</span><span class="sxs-lookup"><span data-stu-id="4b233-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b233-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b233-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b233-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b233-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b233-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b233-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b233-124">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="4b233-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="4b233-125">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="4b233-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="4b233-126">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="4b233-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4b233-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="4b233-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b233-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="4b233-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="4b233-129">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="4b233-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




