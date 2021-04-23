---
description: Указывает URL-адрес для получения лицензии на зашифрованный файл расширенных систем формата (ASF). Этот атрибут соответствует полю "URL-адрес лицензии" заголовка шифрования содержимого, определенного в спецификации ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: Атрибут MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497367"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a><span data-ttu-id="94910-104">\_ \_ \_ \_ \_ Атрибут URL-адреса лицензии MF PD ASF контентенкриптион</span><span class="sxs-lookup"><span data-stu-id="94910-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_LICENSE\_URL attribute</span></span>

<span data-ttu-id="94910-105">Указывает URL-адрес для получения лицензии на зашифрованный файл расширенных систем формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="94910-105">Specifies the license acquisition URL for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="94910-106">Этот атрибут соответствует полю "URL-адрес лицензии" заголовка шифрования содержимого, определенного в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="94910-106">This attribute corresponds to the License URL field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="94910-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="94910-107">Data type</span></span>

<span data-ttu-id="94910-108">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="94910-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="94910-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94910-109">Remarks</span></span>

<span data-ttu-id="94910-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="94910-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="94910-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) извлекает поле URL-адреса лицензии, преобразует его в строку расширенных символов, а затем заполняет массив типа **WCHAR** с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="94910-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the License URL field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="94910-112">Размер массива равен значению поля Длина URL-адреса лицензии в заголовке шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="94910-112">The size of the array equals the License URL Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="94910-113">Требования</span><span class="sxs-lookup"><span data-stu-id="94910-113">Requirements</span></span>



| <span data-ttu-id="94910-114">Требование</span><span class="sxs-lookup"><span data-stu-id="94910-114">Requirement</span></span> | <span data-ttu-id="94910-115">Значение</span><span class="sxs-lookup"><span data-stu-id="94910-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="94910-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94910-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94910-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94910-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="94910-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94910-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94910-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94910-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="94910-120">Header</span><span class="sxs-lookup"><span data-stu-id="94910-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="94910-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="94910-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94910-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94910-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94910-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94910-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94910-124">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="94910-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="94910-125">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="94910-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="94910-126">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="94910-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="94910-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="94910-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="94910-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="94910-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="94910-129">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="94910-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




