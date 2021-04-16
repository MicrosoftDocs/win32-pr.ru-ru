---
description: 'Содержит URL-адрес файла ИФО (сведения о DVD-диске), заданный HTTP-сервером в заголовке HTTP &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Атрибут MF_BYTESTREAM_IFO_FILE_URI (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683123"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="3d67e-103">\_ \_ \_ Атрибут URI файла ИФО MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="3d67e-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="3d67e-104">Содержит URL-адрес файла ИФО (сведения о DVD-диске), заданный HTTP-сервером в заголовке HTTP, "pragma: ifoFileURI.dlna.org".</span><span class="sxs-lookup"><span data-stu-id="3d67e-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="3d67e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3d67e-105">Data type</span></span>

<span data-ttu-id="3d67e-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d67e-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="3d67e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="3d67e-107">Get/set</span></span>

<span data-ttu-id="3d67e-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="3d67e-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="3d67e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="3d67e-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3d67e-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="3d67e-110">Applies to</span></span>

[<span data-ttu-id="3d67e-111">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="3d67e-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="3d67e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d67e-112">Remarks</span></span>

<span data-ttu-id="3d67e-113">Поток байтов HTTP выполняет поиск строки "ifoFileURI.dlna.org" в заголовке HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d67e-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="3d67e-114">Если строка найдена, она копируется в этот атрибут потока байтов.</span><span class="sxs-lookup"><span data-stu-id="3d67e-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="3d67e-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3d67e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d67e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3d67e-116">Requirements</span></span>



| <span data-ttu-id="3d67e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3d67e-117">Requirement</span></span> | <span data-ttu-id="3d67e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d67e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d67e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d67e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d67e-120">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3d67e-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="3d67e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d67e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d67e-122">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3d67e-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="3d67e-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d67e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d67e-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d67e-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d67e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d67e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d67e-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d67e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d67e-127">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="3d67e-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d67e-128">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="3d67e-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




