---
description: Указывает список битовых ставок и соответствующих окон буфера для файла с переменным битом (VBR) расширенного формата системы (ASF).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Атрибут MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712328"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="a05f3-103">\_ \_ \_ \_ \_ Атрибут пар контейнеров утечки метаданных MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="a05f3-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="a05f3-104">Указывает список битовых ставок и соответствующих окон буфера для файла с переменным битом (VBR) расширенного формата системы (ASF).</span><span class="sxs-lookup"><span data-stu-id="a05f3-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a05f3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a05f3-105">Data type</span></span>

<span data-ttu-id="a05f3-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="a05f3-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a05f3-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a05f3-107">Remarks</span></span>

<span data-ttu-id="a05f3-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="a05f3-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a05f3-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут, который применяется к дескриптору представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="a05f3-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="a05f3-110">Значение атрибута имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a05f3-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="a05f3-111">Структура **\_ \_ \_ пары контейнеров с утечками WM** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a05f3-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="a05f3-112">Для каждой скорости потока элемент **мсбуффервиндов** указывает, сколько содержимого буферизовано до начала воспроизведения, в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="a05f3-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="a05f3-113">Размер буфера в байтах равен **мсбуффервинов** x **двбитрате** /8000.</span><span class="sxs-lookup"><span data-stu-id="a05f3-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="a05f3-114">Этот атрибут соответствует атрибуту **асфлеакибуккетпаирс** в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a05f3-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a05f3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a05f3-115">Requirements</span></span>



| <span data-ttu-id="a05f3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a05f3-116">Requirement</span></span> | <span data-ttu-id="a05f3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a05f3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a05f3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a05f3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a05f3-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a05f3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a05f3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a05f3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a05f3-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a05f3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a05f3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a05f3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05f3-123"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05f3-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05f3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a05f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05f3-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a05f3-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a05f3-126">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="a05f3-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a05f3-127">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a05f3-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a05f3-128">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="a05f3-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a05f3-129">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="a05f3-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a05f3-130">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="a05f3-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a05f3-131">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="a05f3-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




