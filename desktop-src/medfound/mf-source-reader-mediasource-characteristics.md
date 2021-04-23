---
description: Возвращает характеристики источника мультимедиа от модуля чтения исходного кода.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Атрибут MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351712"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="da26e-103">\_ \_ \_ Атрибут характеристик медиасаурце для СЧИТЫВАНИя источника MF \_</span><span class="sxs-lookup"><span data-stu-id="da26e-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="da26e-104">Возвращает характеристики источника мультимедиа от [модуля чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="da26e-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="da26e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="da26e-105">Data type</span></span>

<span data-ttu-id="da26e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="da26e-106">**UINT32**</span></span>

<span data-ttu-id="da26e-107">Значение представляет собой побитовое **или** для флагов перечисления [**мфмедиасаурце \_ характеристик**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="da26e-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="da26e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da26e-108">Remarks</span></span>

<span data-ttu-id="da26e-109">Чтобы получить этот атрибут, вызовите метод [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) в модуле чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="da26e-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="da26e-110">Задайте для параметра *двстреаминдекс* значение **MF \_ \_ Reader source \_ медиасаурце** , а параметр *guidAttribute* — значение MF \_ source \_ Reader \_ медиасаурце \_ характеристики.</span><span class="sxs-lookup"><span data-stu-id="da26e-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="da26e-111">Тип **пропвариант** для этого атрибута — **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="da26e-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="da26e-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="da26e-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="da26e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da26e-113">Requirements</span></span>



| <span data-ttu-id="da26e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da26e-114">Requirement</span></span> | <span data-ttu-id="da26e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da26e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da26e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da26e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da26e-117">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="da26e-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="da26e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da26e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da26e-119">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="da26e-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="da26e-120">Header</span><span class="sxs-lookup"><span data-stu-id="da26e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da26e-121"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="da26e-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da26e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da26e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da26e-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da26e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="da26e-124">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="da26e-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




