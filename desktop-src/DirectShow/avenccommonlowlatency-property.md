---
description: Указывает, должен ли выходной поток быть структурирован таким образом, чтобы закодированный поток наменялся с низкой задержкой декодирования.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Свойство Авенккоммонловлатенци (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262466"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="b1782-103">Авенккоммонловлатенци, свойство</span><span class="sxs-lookup"><span data-stu-id="b1782-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="b1782-104">Указывает, должен ли выходной поток быть структурирован таким образом, чтобы закодированный поток наменялся с низкой задержкой декодирования.</span><span class="sxs-lookup"><span data-stu-id="b1782-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="b1782-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b1782-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1782-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b1782-106">Data type</span></span>

<span data-ttu-id="b1782-107">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="b1782-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b1782-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="b1782-108">Property GUID</span></span>

<span data-ttu-id="b1782-109">**КОДЕКАПИ \_ авенккоммонловлатенци**</span><span class="sxs-lookup"><span data-stu-id="b1782-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="b1782-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1782-110">Remarks</span></span>

<span data-ttu-id="b1782-111">Задержка декодирования определяется как объем данных, которые декодер должен забуферировать.</span><span class="sxs-lookup"><span data-stu-id="b1782-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="b1782-112">Например, установка этого свойства в значение **\_ true** в кодировщике видео MPEG ОГРАНИЧИВАЕТ типы структур GOP, которые может использовать кодировщик.</span><span class="sxs-lookup"><span data-stu-id="b1782-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1782-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b1782-113">Requirements</span></span>



| <span data-ttu-id="b1782-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b1782-114">Requirement</span></span> | <span data-ttu-id="b1782-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b1782-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1782-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1782-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1782-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b1782-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b1782-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1782-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1782-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="b1782-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b1782-120">Header</span><span class="sxs-lookup"><span data-stu-id="b1782-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1782-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1782-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1782-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1782-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1782-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="b1782-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b1782-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="b1782-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




