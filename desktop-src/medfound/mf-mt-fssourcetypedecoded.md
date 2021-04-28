---
description: MF_MT_FSSourceTypeDecoded атрибут — указывает, может ли декодер использовать отметки времени декодирования (DTS) при установке меток времени.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093092"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="263c8-103">\_Атрибут MF MT \_ фссаурцетипедекодед</span><span class="sxs-lookup"><span data-stu-id="263c8-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="263c8-104">Указывает, что тип носителя является декодированным.</span><span class="sxs-lookup"><span data-stu-id="263c8-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="263c8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="263c8-105">Data type</span></span>

<span data-ttu-id="263c8-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="263c8-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="263c8-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="263c8-107">Remarks</span></span>
<span data-ttu-id="263c8-108">Тип мультимедиа помечен атрибутом, указывающим, что он не существует в физическом источнике и синтезирован конвейером.</span><span class="sxs-lookup"><span data-stu-id="263c8-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="263c8-109">Значение 1 (TRUE) указывает, что тип носителя является синтезированным.</span><span class="sxs-lookup"><span data-stu-id="263c8-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="263c8-110">Значение 0 (FALSE) или значение отсутствует, указывает, что это не так.</span><span class="sxs-lookup"><span data-stu-id="263c8-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="263c8-111">В текущем выпуске этот атрибут должен быть указан с использованием следующего значения GUID, а не MD_MT_FSSourceTypeDecoded константы:</span><span class="sxs-lookup"><span data-stu-id="263c8-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="263c8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="263c8-112">Requirements</span></span>



| <span data-ttu-id="263c8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="263c8-113">Requirement</span></span> | <span data-ttu-id="263c8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="263c8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="263c8-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="263c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="263c8-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="263c8-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="263c8-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="263c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="263c8-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="263c8-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="263c8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="263c8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263c8-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="263c8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




