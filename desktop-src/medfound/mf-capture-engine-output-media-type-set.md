---
description: 'Указывает, что тип выходных данных был установлен в подсистеме отслеживания в ответ на IMFCaptureSink2:: Сетаутпуттипе.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Атрибут MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351645"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a><span data-ttu-id="b83c2-103">\_ \_ \_ Тип выходного \_ \_ \_ набора данных обработчика записи MF</span><span class="sxs-lookup"><span data-stu-id="b83c2-103">MF\_CAPTURE\_ENGINE\_OUTPUT\_MEDIA\_TYPE\_SET attribute</span></span>

<span data-ttu-id="b83c2-104">Указывает, что тип выходных данных был установлен в подсистеме отслеживания в ответ на [**IMFCaptureSink2:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="b83c2-104">Indicates that the output type has been set on the capture engine in response to [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="data-type"></a><span data-ttu-id="b83c2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b83c2-105">Data type</span></span>

<span data-ttu-id="b83c2-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b83c2-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b83c2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83c2-107">Remarks</span></span>

<span data-ttu-id="b83c2-108">Чтобы выяснить, была ли операция успешной, можно вызвать [**имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="b83c2-108">You can call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) to find out if the operation was successful or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="b83c2-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b83c2-109">Requirements</span></span>



| <span data-ttu-id="b83c2-110">Требование</span><span class="sxs-lookup"><span data-stu-id="b83c2-110">Requirement</span></span> | <span data-ttu-id="b83c2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b83c2-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b83c2-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b83c2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b83c2-113">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b83c2-113">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b83c2-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b83c2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b83c2-115">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b83c2-115">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b83c2-116">Header</span><span class="sxs-lookup"><span data-stu-id="b83c2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b83c2-117"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="b83c2-117"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="b83c2-118">IDL</span><span class="sxs-lookup"><span data-stu-id="b83c2-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b83c2-119"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b83c2-119"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b83c2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b83c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83c2-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b83c2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b83c2-122">**IMFCaptureSink2:: Сетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="b83c2-122">**IMFCaptureSink2::SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




