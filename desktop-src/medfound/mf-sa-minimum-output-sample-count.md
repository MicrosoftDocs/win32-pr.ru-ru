---
description: Указывает максимальное количество выходных образцов, которые преMicrosoft Media Foundation преобразование MFT в любой момент времени будут ожидать в конвейере.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Атрибут MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263363"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="80526-103">\_ \_ \_ \_ Атрибут счетчика выборки МИНИМАЛЬного значения SA \_ MF</span><span class="sxs-lookup"><span data-stu-id="80526-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="80526-104">Указывает максимальное количество выходных образцов, которые преMicrosoft Media Foundation преобразование MFT в любой момент времени будут ожидать в конвейере.</span><span class="sxs-lookup"><span data-stu-id="80526-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="80526-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80526-105">Data type</span></span>

<span data-ttu-id="80526-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="80526-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="80526-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80526-107">Remarks</span></span>

<span data-ttu-id="80526-108">Этот атрибут применяется только к МФТС, в котором для выделения собственных выходных образцов используется круглый буфер.</span><span class="sxs-lookup"><span data-stu-id="80526-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="80526-109">Другие МФТС игнорируют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="80526-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="80526-110">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="80526-110">To set this attribute:</span></span>

1.  <span data-ttu-id="80526-111">Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="80526-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="80526-112">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы добавить атрибут.</span><span class="sxs-lookup"><span data-stu-id="80526-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="80526-113">Требования</span><span class="sxs-lookup"><span data-stu-id="80526-113">Requirements</span></span>



| <span data-ttu-id="80526-114">Требование</span><span class="sxs-lookup"><span data-stu-id="80526-114">Requirement</span></span> | <span data-ttu-id="80526-115">Значение</span><span class="sxs-lookup"><span data-stu-id="80526-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80526-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80526-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80526-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="80526-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="80526-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80526-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80526-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="80526-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="80526-120">Header</span><span class="sxs-lookup"><span data-stu-id="80526-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80526-121"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="80526-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80526-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80526-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80526-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80526-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80526-124">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="80526-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




