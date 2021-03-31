---
description: Содержит указатель Имффиелдофусемфтунлокк, который можно использовать для разблокировки преобразования Media Foundation (MFT). Интерфейс Имффиелдофусемфтунлокк используется для разблокировки MFT с ограничениями на использование полей.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Атрибут MFT_FIELDOFUSE_UNLOCK_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812604"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="87e62-104">\_Атрибут фиелдофусе \_ Unlock атрибута MFT \_</span><span class="sxs-lookup"><span data-stu-id="87e62-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="87e62-105">Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который можно использовать для разблокировки преобразования Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="87e62-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="87e62-106">Интерфейс **имффиелдофусемфтунлокк** используется для разблокировки MFT с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="87e62-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="87e62-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="87e62-107">Data type</span></span>

<span data-ttu-id="87e62-108">**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) Имффиелдофусемфтунлокк \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="87e62-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="87e62-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="87e62-109">Get/set</span></span>

<span data-ttu-id="87e62-110">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="87e62-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="87e62-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="87e62-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="87e62-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87e62-112">Remarks</span></span>

<span data-ttu-id="87e62-113">Дополнительные сведения об этом атрибуте см. в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="87e62-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="87e62-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="87e62-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e62-115">Требования</span><span class="sxs-lookup"><span data-stu-id="87e62-115">Requirements</span></span>



| <span data-ttu-id="87e62-116">Требование</span><span class="sxs-lookup"><span data-stu-id="87e62-116">Requirement</span></span> | <span data-ttu-id="87e62-117">Значение</span><span class="sxs-lookup"><span data-stu-id="87e62-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e62-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87e62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87e62-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="87e62-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="87e62-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87e62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87e62-121">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="87e62-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="87e62-122">Header</span><span class="sxs-lookup"><span data-stu-id="87e62-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87e62-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e62-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e62-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87e62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e62-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87e62-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="87e62-126">Поле ограничений использования</span><span class="sxs-lookup"><span data-stu-id="87e62-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="87e62-127">**мфкреатетрансформактивате**</span><span class="sxs-lookup"><span data-stu-id="87e62-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




