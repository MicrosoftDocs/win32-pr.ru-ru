---
description: Указывает дату и время создания файла расширенных систем форматирования (ASF).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Атрибут MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991089"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="bdf2e-103">\_ \_ \_ \_ Атрибут времени создания MF PD ASF филепропертиес \_</span><span class="sxs-lookup"><span data-stu-id="bdf2e-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="bdf2e-104">Указывает дату и время создания файла расширенных систем форматирования (ASF).</span><span class="sxs-lookup"><span data-stu-id="bdf2e-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="bdf2e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bdf2e-105">Data type</span></span>

<span data-ttu-id="bdf2e-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="bdf2e-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf2e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdf2e-107">Remarks</span></span>

<span data-ttu-id="bdf2e-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="bdf2e-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="bdf2e-109">Значением атрибута является структура **fileTime** , которая описана в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bdf2e-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="bdf2e-110">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="bdf2e-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf2e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bdf2e-111">Requirements</span></span>



| <span data-ttu-id="bdf2e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bdf2e-112">Requirement</span></span> | <span data-ttu-id="bdf2e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf2e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf2e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdf2e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf2e-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdf2e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bdf2e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdf2e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf2e-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bdf2e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bdf2e-118">Header</span><span class="sxs-lookup"><span data-stu-id="bdf2e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf2e-119"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf2e-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf2e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdf2e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf2e-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdf2e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bdf2e-122">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="bdf2e-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="bdf2e-123">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="bdf2e-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="bdf2e-124">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="bdf2e-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="bdf2e-125">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="bdf2e-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bdf2e-126">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="bdf2e-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bdf2e-127">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="bdf2e-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




