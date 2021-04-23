---
description: Указывает тип механизма защиты, используемого в расширенном файле формата Systems (ASF).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Атрибут MF_PD_ASF_CONTENTENCRYPTION_TYPE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897269"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="80cea-103">\_ \_ \_ Атрибут типа контентенкриптион MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="80cea-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="80cea-104">Указывает тип механизма защиты, используемого в расширенном файле формата Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="80cea-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="80cea-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80cea-105">Data type</span></span>

<span data-ttu-id="80cea-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="80cea-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="80cea-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80cea-107">Remarks</span></span>

<span data-ttu-id="80cea-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="80cea-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="80cea-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) извлекает поле типа защиты, преобразует его в строку расширенных символов, а затем заполняет массив типа **WCHAR** с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="80cea-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="80cea-110">При наличии значение должно быть "DRM".</span><span class="sxs-lookup"><span data-stu-id="80cea-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="80cea-111">Размер массива равен полю "Длина поля типа защиты" заголовка шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="80cea-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="80cea-112">Требования</span><span class="sxs-lookup"><span data-stu-id="80cea-112">Requirements</span></span>



| <span data-ttu-id="80cea-113">Требование</span><span class="sxs-lookup"><span data-stu-id="80cea-113">Requirement</span></span> | <span data-ttu-id="80cea-114">Значение</span><span class="sxs-lookup"><span data-stu-id="80cea-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cea-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80cea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="80cea-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80cea-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80cea-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80cea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="80cea-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80cea-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="80cea-119">Header</span><span class="sxs-lookup"><span data-stu-id="80cea-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="80cea-120"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="80cea-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80cea-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80cea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80cea-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80cea-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80cea-123">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="80cea-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="80cea-124">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="80cea-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="80cea-125">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="80cea-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="80cea-126">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="80cea-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="80cea-127">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="80cea-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="80cea-128">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="80cea-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




