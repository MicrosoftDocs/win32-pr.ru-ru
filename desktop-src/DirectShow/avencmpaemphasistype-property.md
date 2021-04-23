---
description: Указывает тип фильтра отмены выделения, который должен использоваться при декодировании. Это свойство применяется к кодировщикам аудио в формате MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Свойство Авенкмпаемфасистипе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682264"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="3ad39-104">Авенкмпаемфасистипе, свойство</span><span class="sxs-lookup"><span data-stu-id="3ad39-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="3ad39-105">Указывает тип фильтра отмены выделения, который должен использоваться при декодировании.</span><span class="sxs-lookup"><span data-stu-id="3ad39-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="3ad39-106">Это свойство применяется к кодировщикам аудио в формате MPEG.</span><span class="sxs-lookup"><span data-stu-id="3ad39-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="3ad39-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3ad39-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ad39-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3ad39-108">Data type</span></span>

<span data-ttu-id="3ad39-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3ad39-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3ad39-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="3ad39-110">Property GUID</span></span>

<span data-ttu-id="3ad39-111">**КОДЕКАПИ \_ авенкмпаемфасистипе**</span><span class="sxs-lookup"><span data-stu-id="3ad39-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="3ad39-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3ad39-112">Property value</span></span>

<span data-ttu-id="3ad39-113">Значение этого свойства является членом перечисления [**еавенкмпаемфасистипе**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .</span><span class="sxs-lookup"><span data-stu-id="3ad39-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad39-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ad39-114">Remarks</span></span>

<span data-ttu-id="3ad39-115">Это свойство задает биты выделения в заголовке фрейма.</span><span class="sxs-lookup"><span data-stu-id="3ad39-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad39-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3ad39-116">Requirements</span></span>



| <span data-ttu-id="3ad39-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3ad39-117">Requirement</span></span> | <span data-ttu-id="3ad39-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3ad39-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad39-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ad39-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad39-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ad39-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3ad39-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ad39-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad39-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ad39-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3ad39-123">Header</span><span class="sxs-lookup"><span data-stu-id="3ad39-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad39-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad39-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad39-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ad39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad39-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="3ad39-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3ad39-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="3ad39-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

