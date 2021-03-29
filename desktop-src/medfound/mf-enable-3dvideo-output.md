---
description: Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Атрибут MF_ENABLE_3DVIDEO_OUTPUT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898358"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="1147f-103">\_Включить \_ \_ выходной атрибут 3DVIDEO MF</span><span class="sxs-lookup"><span data-stu-id="1147f-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="1147f-104">Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.</span><span class="sxs-lookup"><span data-stu-id="1147f-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1147f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1147f-105">Data type</span></span>

<span data-ttu-id="1147f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1147f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1147f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1147f-107">Remarks</span></span>

<span data-ttu-id="1147f-108">Значение атрибута является членом перечисления [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .</span><span class="sxs-lookup"><span data-stu-id="1147f-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="1147f-109">Этот атрибут применяется только в том случае, если MFT возвращает **значение true** для атрибута [ \_ \_ 3DVIDEO поддержки MFT](mft-support-3dvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="1147f-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="1147f-110">Чтобы получить или задать этот атрибут, необходимо вызвать [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="1147f-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="1147f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1147f-111">Requirements</span></span>



| <span data-ttu-id="1147f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1147f-112">Requirement</span></span> | <span data-ttu-id="1147f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1147f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1147f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1147f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1147f-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1147f-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1147f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1147f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1147f-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1147f-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1147f-118">Header</span><span class="sxs-lookup"><span data-stu-id="1147f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1147f-119"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="1147f-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1147f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1147f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1147f-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1147f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




