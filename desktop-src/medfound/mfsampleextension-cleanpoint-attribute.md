---
description: Указывает, является ли образец точкой доступа случайным образом.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: Атрибут MFSampleExtension_CleanPoint (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543954"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="197c2-103">Мфсампликстенсион \_ клеанпоинт, атрибут</span><span class="sxs-lookup"><span data-stu-id="197c2-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="197c2-104">Указывает, является ли образец точкой доступа случайным образом.</span><span class="sxs-lookup"><span data-stu-id="197c2-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="197c2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="197c2-105">Data type</span></span>

<span data-ttu-id="197c2-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="197c2-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="197c2-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="197c2-107">Get/set</span></span>

<span data-ttu-id="197c2-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="197c2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="197c2-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="197c2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="197c2-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="197c2-110">Applies to</span></span>

[<span data-ttu-id="197c2-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="197c2-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="197c2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="197c2-112">Remarks</span></span>

<span data-ttu-id="197c2-113">Этот атрибут применяется к примерам.</span><span class="sxs-lookup"><span data-stu-id="197c2-113">This attribute applies to samples.</span></span> <span data-ttu-id="197c2-114">Если атрибут имеет **значение true**, то образец является случайной точкой доступа и декодированием, который может начаться из этого примера.</span><span class="sxs-lookup"><span data-stu-id="197c2-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="197c2-115">В противном случае образец не является случайной точкой доступа.</span><span class="sxs-lookup"><span data-stu-id="197c2-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="197c2-116">Если этот атрибут не задан, по умолчанию используется значение **false**.</span><span class="sxs-lookup"><span data-stu-id="197c2-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="197c2-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="197c2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="197c2-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="197c2-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="197c2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="197c2-119">Requirements</span></span>



| <span data-ttu-id="197c2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="197c2-120">Requirement</span></span> | <span data-ttu-id="197c2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="197c2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="197c2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="197c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="197c2-123">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="197c2-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="197c2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="197c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="197c2-125">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="197c2-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="197c2-126">Header</span><span class="sxs-lookup"><span data-stu-id="197c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="197c2-127"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="197c2-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197c2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="197c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197c2-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="197c2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="197c2-130">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="197c2-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="197c2-131">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="197c2-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




