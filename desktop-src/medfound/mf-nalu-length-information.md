---
description: Указывает длину Налус в образце. Это большой двоичный объект MF, заданный в сжатых примерах входных данных для декодера H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Атрибут MF_NALU_LENGTH_INFORMATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692930"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="02447-104">\_ \_ Атрибут сведений о длине MF налу \_</span><span class="sxs-lookup"><span data-stu-id="02447-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="02447-105">Указывает длину Налус в образце.</span><span class="sxs-lookup"><span data-stu-id="02447-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="02447-106">Это **большой двоичный объект** MF, заданный в сжатых примерах входных данных для декодера H. 264.</span><span class="sxs-lookup"><span data-stu-id="02447-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="02447-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="02447-107">Data type</span></span>

<span data-ttu-id="02447-108">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="02447-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="02447-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02447-109">Remarks</span></span>

<span data-ttu-id="02447-110">Чтобы задать этот атрибут, носитель должен иметь тип МЕДИАСУБТИПЕ \_ H264 Single bitrate, а для входного типа носителя медиасубтипе H264 Single bitrate должен быть задан атрибут [ \_ длины MF налу \_ length \_ ](mf-nalu-length-set.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="02447-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="02447-111">Задайте \_ \_ сведения о длине MF налу в \_ виде **большого двоичного объекта** в примере входных данных с одним DWORD для каждого налу в образце.</span><span class="sxs-lookup"><span data-stu-id="02447-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="02447-112">Например, если имеется AUD (9 байт), SPS (25 байт), PPS (10 байт), IDR slice1 (50 k), IDR Slice 2 (60 k), то в **BLOB-объекте** должно быть 5 DWORD со значениями 9, 25, 10, 50 k и 60 k.</span><span class="sxs-lookup"><span data-stu-id="02447-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="02447-113">Ниже приведен код, задающий **большой двоичный объект**, где **ргдвналуленгсинфо** — массив типа DWORD, а **УИНАЛУЛЕНГСИДКС** — допустимая длина налу, установленная для **большого двоичного объекта**.</span><span class="sxs-lookup"><span data-stu-id="02447-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="02447-114">Требования</span><span class="sxs-lookup"><span data-stu-id="02447-114">Requirements</span></span>



| <span data-ttu-id="02447-115">Требование</span><span class="sxs-lookup"><span data-stu-id="02447-115">Requirement</span></span> | <span data-ttu-id="02447-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02447-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02447-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02447-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02447-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="02447-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="02447-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02447-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02447-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="02447-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="02447-121">Header</span><span class="sxs-lookup"><span data-stu-id="02447-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02447-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="02447-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02447-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02447-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02447-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02447-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02447-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="02447-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




