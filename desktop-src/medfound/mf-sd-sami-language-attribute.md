---
description: Содержит имя языка для синхронизированного доступного обмена мультимедиа (SAMI), определенное для потока.
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: Атрибут MF_SD_SAMI_LANGUAGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712908"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="9027e-103">\_ \_ Атрибут языка MF SD Sami \_</span><span class="sxs-lookup"><span data-stu-id="9027e-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="9027e-104">Содержит имя языка для синхронизированного доступного обмена мультимедиа (SAMI), определенное для потока.</span><span class="sxs-lookup"><span data-stu-id="9027e-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="9027e-105">Этот атрибут имеется в дескрипторах потока, возвращаемых источником носителя SAMI.</span><span class="sxs-lookup"><span data-stu-id="9027e-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9027e-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9027e-106">Data type</span></span>

<span data-ttu-id="9027e-107">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="9027e-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="9027e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9027e-108">Remarks</span></span>

<span data-ttu-id="9027e-109">Имя языка SAMI указывается в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="9027e-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="9027e-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9027e-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9027e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9027e-111">Requirements</span></span>



| <span data-ttu-id="9027e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9027e-112">Requirement</span></span> | <span data-ttu-id="9027e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9027e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9027e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9027e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9027e-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9027e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9027e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9027e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9027e-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9027e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9027e-118">Header</span><span class="sxs-lookup"><span data-stu-id="9027e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9027e-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9027e-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9027e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9027e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9027e-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9027e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9027e-122">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="9027e-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="9027e-123">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="9027e-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="9027e-124">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="9027e-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="9027e-125">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="9027e-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="9027e-126">**имфсамистиле**</span><span class="sxs-lookup"><span data-stu-id="9027e-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




