---
description: Указывает минимальное количество последовательных выборок, которые Microsoft Media Foundation преобразование (MFT) должны допускать аустандинг в любое заданное время.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Атрибут MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265356"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="6573b-103">\_ \_ \_ Последовательное значение \_ \_ счетчика минимального количества выходных данных SA \_ MF</span><span class="sxs-lookup"><span data-stu-id="6573b-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="6573b-104">Указывает минимальное количество последовательных выборок, которые Microsoft Media Foundation преобразование (MFT) должны допускать аустандинг в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="6573b-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="6573b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6573b-105">Data type</span></span>

<span data-ttu-id="6573b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6573b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6573b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6573b-107">Remarks</span></span>

<span data-ttu-id="6573b-108">Этот атрибут применяется только к МФТС, в котором для выделения собственных выходных образцов используется круглый буфер.</span><span class="sxs-lookup"><span data-stu-id="6573b-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="6573b-109">Другие МФТС игнорируют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="6573b-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="6573b-110">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="6573b-110">To set this attribute:</span></span>

1.  <span data-ttu-id="6573b-111">Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="6573b-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="6573b-112">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы добавить атрибут.</span><span class="sxs-lookup"><span data-stu-id="6573b-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6573b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6573b-113">Requirements</span></span>



| <span data-ttu-id="6573b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6573b-114">Requirement</span></span> | <span data-ttu-id="6573b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6573b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6573b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6573b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6573b-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="6573b-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6573b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6573b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6573b-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6573b-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6573b-120">Header</span><span class="sxs-lookup"><span data-stu-id="6573b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6573b-121"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="6573b-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6573b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6573b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6573b-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6573b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




