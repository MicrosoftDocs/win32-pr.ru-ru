---
description: Указывает, может ли декодер использовать метки времени декодирования (DTS) при установке меток времени.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719742"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="33e94-103">\_Атрибут MF MT \_ фссаурцетипедекодед</span><span class="sxs-lookup"><span data-stu-id="33e94-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="33e94-104">Указывает, что тип носителя является декодированным.</span><span class="sxs-lookup"><span data-stu-id="33e94-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="33e94-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="33e94-105">Data type</span></span>

<span data-ttu-id="33e94-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="33e94-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="33e94-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33e94-107">Remarks</span></span>
<span data-ttu-id="33e94-108">Тип мультимедиа помечен атрибутом, указывающим, что он не существует в физическом источнике и синтезирован конвейером.</span><span class="sxs-lookup"><span data-stu-id="33e94-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="33e94-109">Значение 1 (TRUE) указывает, что тип носителя является синтезированным.</span><span class="sxs-lookup"><span data-stu-id="33e94-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="33e94-110">Значение 0 (FALSE) или значение отсутствует, указывает, что это не так.</span><span class="sxs-lookup"><span data-stu-id="33e94-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="33e94-111">В текущем выпуске этот атрибут должен быть указан с использованием следующего значения GUID, а не MD_MT_FSSourceTypeDecoded константы:</span><span class="sxs-lookup"><span data-stu-id="33e94-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="33e94-112">Требования</span><span class="sxs-lookup"><span data-stu-id="33e94-112">Requirements</span></span>



| <span data-ttu-id="33e94-113">Требование</span><span class="sxs-lookup"><span data-stu-id="33e94-113">Requirement</span></span> | <span data-ttu-id="33e94-114">Значение</span><span class="sxs-lookup"><span data-stu-id="33e94-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33e94-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33e94-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33e94-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="33e94-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="33e94-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33e94-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33e94-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="33e94-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="33e94-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33e94-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e94-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33e94-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




