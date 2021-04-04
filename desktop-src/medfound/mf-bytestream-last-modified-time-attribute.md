---
description: Указывает, когда байтовый поток был изменен в последний раз.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: Атрибут MF_BYTESTREAM_LAST_MODIFIED_TIME (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811861"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="c6099-103">\_ \_ \_ Атрибут времени последнего изменения MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="c6099-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="c6099-104">Указывает, когда байтовый поток был изменен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="c6099-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6099-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c6099-105">Data type</span></span>

<span data-ttu-id="c6099-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="c6099-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c6099-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6099-107">Remarks</span></span>

<span data-ttu-id="c6099-108">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c6099-108">This attribute is optional.</span></span> <span data-ttu-id="c6099-109">Значением атрибута является структура [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="c6099-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="c6099-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="c6099-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6099-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c6099-111">Requirements</span></span>



| <span data-ttu-id="c6099-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c6099-112">Requirement</span></span> | <span data-ttu-id="c6099-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c6099-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6099-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6099-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c6099-115">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c6099-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c6099-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6099-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c6099-117">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c6099-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c6099-118">Header</span><span class="sxs-lookup"><span data-stu-id="c6099-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6099-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6099-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6099-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6099-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6099-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6099-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6099-122">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="c6099-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6099-123">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="c6099-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c6099-124">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="c6099-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c6099-125">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="c6099-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
