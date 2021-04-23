---
description: Задает идентификатор ключа для образца.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Атрибут MFSampleExtension_Content_KeyID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662779"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="7e783-103">\_ \_ Атрибут KeyID Content мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="7e783-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="7e783-104">Задает идентификатор ключа для образца.</span><span class="sxs-lookup"><span data-stu-id="7e783-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e783-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7e783-105">Data type</span></span>

<span data-ttu-id="7e783-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7e783-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="7e783-107">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e783-107">Examples</span></span>

<span data-ttu-id="7e783-108">В следующем примере показано, как задать идентификатор ключа для образца.</span><span class="sxs-lookup"><span data-stu-id="7e783-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="7e783-109">Требования</span><span class="sxs-lookup"><span data-stu-id="7e783-109">Requirements</span></span>



| <span data-ttu-id="7e783-110">Требование</span><span class="sxs-lookup"><span data-stu-id="7e783-110">Requirement</span></span> | <span data-ttu-id="7e783-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7e783-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e783-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e783-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7e783-113">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="7e783-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7e783-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e783-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7e783-115">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7e783-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e783-116">Header</span><span class="sxs-lookup"><span data-stu-id="7e783-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e783-117"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e783-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e783-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e783-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e783-119">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e783-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e783-120">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="7e783-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="7e783-121">\_Субсамплемаппингсплит шифрования \_ мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="7e783-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




