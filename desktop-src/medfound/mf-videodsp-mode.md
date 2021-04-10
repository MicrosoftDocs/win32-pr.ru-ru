---
description: Задает режим обработки Стабилизация видео MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Атрибут MF_VIDEODSP_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154974"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="69075-103">\_ \_ Атрибут режима видеодсп MF</span><span class="sxs-lookup"><span data-stu-id="69075-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="69075-104">Задает режим обработки [**стабилизация видео MFT**](video-stabilization-mft.md).</span><span class="sxs-lookup"><span data-stu-id="69075-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="69075-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="69075-105">Data type</span></span>

<span data-ttu-id="69075-106">**Мфвидеодспмоде** хранится в виде **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="69075-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="69075-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69075-107">Remarks</span></span>

<span data-ttu-id="69075-108">Значением этого атрибута является значение перечисления [**мфвидеодспмоде**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="69075-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="69075-109">Этот атрибут можно использовать для включения или отключения образа стабилизации и может быть обновлен для каждого образца выходных данных.</span><span class="sxs-lookup"><span data-stu-id="69075-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="69075-110">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="69075-110">To set this attribute:</span></span>

1.  <span data-ttu-id="69075-111">Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в файле MFT видео стабилизации, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="69075-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="69075-112">Вызовите метод [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы задать атрибут.</span><span class="sxs-lookup"><span data-stu-id="69075-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="69075-113">Требования</span><span class="sxs-lookup"><span data-stu-id="69075-113">Requirements</span></span>



| <span data-ttu-id="69075-114">Требование</span><span class="sxs-lookup"><span data-stu-id="69075-114">Requirement</span></span> | <span data-ttu-id="69075-115">Значение</span><span class="sxs-lookup"><span data-stu-id="69075-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69075-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69075-116">Minimum supported client</span></span><br/> | <span data-ttu-id="69075-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="69075-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="69075-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69075-118">Minimum supported server</span></span><br/> | <span data-ttu-id="69075-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="69075-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69075-120">Header</span><span class="sxs-lookup"><span data-stu-id="69075-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="69075-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="69075-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69075-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69075-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69075-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69075-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69075-124">**Стабилизация видео MFT**</span><span class="sxs-lookup"><span data-stu-id="69075-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




