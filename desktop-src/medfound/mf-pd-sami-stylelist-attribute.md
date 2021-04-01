---
description: Содержит понятные имена для синхронизированных доступных стилей обмена мультимедийными данными (SAMI), определенных в файле SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Атрибут MF_PD_SAMI_STYLELIST (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913164"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="18bd0-103">\_ \_ Атрибут стилелист MF PD samid \_</span><span class="sxs-lookup"><span data-stu-id="18bd0-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="18bd0-104">Содержит понятные имена для синхронизированных доступных стилей обмена мультимедийными данными (SAMI), определенных в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="18bd0-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="18bd0-105">[Источник носителя Sami](sami-media-source.md) задает этот атрибут для создаваемого дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="18bd0-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="18bd0-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="18bd0-106">Data type</span></span>

<span data-ttu-id="18bd0-107">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="18bd0-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="18bd0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18bd0-108">Remarks</span></span>

<span data-ttu-id="18bd0-109">Большой двоичный объект атрибута имеет следующую структуру:</span><span class="sxs-lookup"><span data-stu-id="18bd0-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="18bd0-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="18bd0-110">Data Type</span></span>

<span data-ttu-id="18bd0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="18bd0-111">Description</span></span>

<span data-ttu-id="18bd0-112">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="18bd0-112">Size (bytes)</span></span>

<span data-ttu-id="18bd0-113">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="18bd0-113">**DWORD**</span></span>

<span data-ttu-id="18bd0-114">Число строк стиля.</span><span class="sxs-lookup"><span data-stu-id="18bd0-114">Number of style strings.</span></span>

<span data-ttu-id="18bd0-115">4</span><span class="sxs-lookup"><span data-stu-id="18bd0-115">4</span></span>

<span data-ttu-id="18bd0-116">Для каждой строки стиля:</span><span class="sxs-lookup"><span data-stu-id="18bd0-116">For each style string:</span></span>

<span data-ttu-id="18bd0-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="18bd0-117">**DWORD**</span></span>

<span data-ttu-id="18bd0-118">Размер строки в байтах, включая символ **null** .</span><span class="sxs-lookup"><span data-stu-id="18bd0-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="18bd0-119">4</span><span class="sxs-lookup"><span data-stu-id="18bd0-119">4</span></span>

<span data-ttu-id="18bd0-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="18bd0-120">**LPWSTR**</span></span>

<span data-ttu-id="18bd0-121">Строка расширенных символов, заканчивающаяся символом NULL, содержащая имя стиля.</span><span class="sxs-lookup"><span data-stu-id="18bd0-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="18bd0-122">Различается</span><span class="sxs-lookup"><span data-stu-id="18bd0-122">Varies</span></span>



 

<span data-ttu-id="18bd0-123">Чтобы задать стиль или получить текущий стиль, используйте интерфейс [**имфсамистиле**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="18bd0-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="18bd0-124">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="18bd0-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="18bd0-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="18bd0-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="18bd0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="18bd0-126">Requirements</span></span>



| <span data-ttu-id="18bd0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="18bd0-127">Requirement</span></span> | <span data-ttu-id="18bd0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="18bd0-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18bd0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18bd0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="18bd0-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18bd0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18bd0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18bd0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="18bd0-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18bd0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18bd0-133">Header</span><span class="sxs-lookup"><span data-stu-id="18bd0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="18bd0-134"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bd0-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18bd0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18bd0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18bd0-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18bd0-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18bd0-137">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="18bd0-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="18bd0-138">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="18bd0-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="18bd0-139">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="18bd0-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="18bd0-140">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="18bd0-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="18bd0-141">Источник носителя SAMI</span><span class="sxs-lookup"><span data-stu-id="18bd0-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




