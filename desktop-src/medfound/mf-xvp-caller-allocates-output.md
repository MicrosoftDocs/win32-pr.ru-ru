---
description: Указывает, будет ли вызывающий объект распределять текстуры, используемые для вывода.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Атрибут MF_XVP_CALLER_ALLOCATES_OUTPUT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543218"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="c7669-103">\_ \_ Вызывающий объект MF ксвп \_ выделяет \_ выходной атрибут</span><span class="sxs-lookup"><span data-stu-id="c7669-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="c7669-104">Указывает, будет ли вызывающий объект распределять текстуры, используемые для вывода.</span><span class="sxs-lookup"><span data-stu-id="c7669-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7669-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c7669-105">Data type</span></span>

<span data-ttu-id="c7669-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c7669-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c7669-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7669-107">Remarks</span></span>

<span data-ttu-id="c7669-108">Если этот атрибут имеет **значение true**, обработчик видео ждет выделения выходных текстур вызывающей стороной, даже если работает в режиме ускорения DirectX Video (дксва).</span><span class="sxs-lookup"><span data-stu-id="c7669-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="c7669-109">Если этот атрибут имеет **значение false**, процессор видео выделит выходные текстуры при работе в режиме дксва и завершится ошибкой, если предоставлены выходные текстуры, предоставленные абонентом.</span><span class="sxs-lookup"><span data-stu-id="c7669-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="c7669-110">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="c7669-110">To set this attribute:</span></span>

1.  <span data-ttu-id="c7669-111">Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в обработчике видео.</span><span class="sxs-lookup"><span data-stu-id="c7669-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="c7669-112">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c7669-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="c7669-113">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="c7669-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7669-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c7669-114">Requirements</span></span>



| <span data-ttu-id="c7669-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c7669-115">Requirement</span></span> | <span data-ttu-id="c7669-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c7669-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7669-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7669-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7669-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c7669-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7669-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7669-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7669-120">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c7669-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c7669-121">Header</span><span class="sxs-lookup"><span data-stu-id="c7669-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7669-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7669-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7669-123">IDL</span><span class="sxs-lookup"><span data-stu-id="c7669-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7669-124"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7669-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7669-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7669-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7669-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7669-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




