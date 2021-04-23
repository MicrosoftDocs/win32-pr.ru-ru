---
description: Указывает, использует ли Имфтрансформ аппаратный DRM.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497763"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="8edcc-103">MFT \_ с использованием \_ аппаратного \_ атрибута DRM</span><span class="sxs-lookup"><span data-stu-id="8edcc-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="8edcc-104">Указывает, использует ли Имфтрансформ аппаратный DRM.</span><span class="sxs-lookup"><span data-stu-id="8edcc-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="8edcc-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8edcc-105">Data type</span></span>

<span data-ttu-id="8edcc-106">**UINT32** (рассматривается как **bool**)</span><span class="sxs-lookup"><span data-stu-id="8edcc-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="8edcc-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="8edcc-107">Get/set</span></span>

<span data-ttu-id="8edcc-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8edcc-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8edcc-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8edcc-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8edcc-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="8edcc-110">Applies to</span></span>

[<span data-ttu-id="8edcc-111">**имтрансфром**</span><span class="sxs-lookup"><span data-stu-id="8edcc-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="8edcc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8edcc-112">Remarks</span></span>

<span data-ttu-id="8edcc-113">Если расшифровка MFT задает для этого атрибута значение 1, то используется аппаратный DRM.</span><span class="sxs-lookup"><span data-stu-id="8edcc-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="8edcc-114">Если расшифровка MFT задает для этого атрибута значение 0, то оборудование DRM не используется.</span><span class="sxs-lookup"><span data-stu-id="8edcc-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="8edcc-115">Если в расшифровке MFT не указан этот атрибут или указано другое значение, то он не (или не может) указать, использует ли он аппаратный DRM.</span><span class="sxs-lookup"><span data-stu-id="8edcc-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="8edcc-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8edcc-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8edcc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8edcc-117">Requirements</span></span>



| <span data-ttu-id="8edcc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8edcc-118">Requirement</span></span> | <span data-ttu-id="8edcc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8edcc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8edcc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8edcc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8edcc-121">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="8edcc-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="8edcc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8edcc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8edcc-123">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="8edcc-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8edcc-124">Header</span><span class="sxs-lookup"><span data-stu-id="8edcc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8edcc-125"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="8edcc-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8edcc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8edcc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edcc-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8edcc-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="8edcc-128">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="8edcc-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




