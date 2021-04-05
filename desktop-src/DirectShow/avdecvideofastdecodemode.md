---
description: Возвращает или задает скорость декодирования видео.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Свойство Авдеквидеофастдекодемоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140495"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="45579-103">Авдеквидеофастдекодемоде, свойство</span><span class="sxs-lookup"><span data-stu-id="45579-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="45579-104">Возвращает или задает скорость декодирования видео.</span><span class="sxs-lookup"><span data-stu-id="45579-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="45579-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="45579-105">Data type</span></span>

<span data-ttu-id="45579-106">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="45579-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="45579-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="45579-107">Property GUID</span></span>

<span data-ttu-id="45579-108">**КОДЕКАПИ \_ авдеквидеофастдекодемоде**</span><span class="sxs-lookup"><span data-stu-id="45579-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="45579-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="45579-109">Property value</span></span>

<span data-ttu-id="45579-110">Значение этого свойства может находиться в диапазоне от 0 до 32, где 0 означает нормальную декодирование, а 32 — самый быстрый режим декодирования.</span><span class="sxs-lookup"><span data-stu-id="45579-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="45579-111">Точное поведение зависит от реализации декодера.</span><span class="sxs-lookup"><span data-stu-id="45579-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="45579-112">Не все значения в диапазоне от 1 до 32 обязательно определяются в разных режимах.</span><span class="sxs-lookup"><span data-stu-id="45579-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="45579-113">Перечисление [**еавфастдекодемоде**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) содержит некоторые предопределенные режимы для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="45579-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="45579-114">Требования</span><span class="sxs-lookup"><span data-stu-id="45579-114">Requirements</span></span>



| <span data-ttu-id="45579-115">Требование</span><span class="sxs-lookup"><span data-stu-id="45579-115">Requirement</span></span> | <span data-ttu-id="45579-116">Значение</span><span class="sxs-lookup"><span data-stu-id="45579-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45579-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45579-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45579-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="45579-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="45579-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45579-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45579-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="45579-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="45579-121">Header</span><span class="sxs-lookup"><span data-stu-id="45579-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="45579-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="45579-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45579-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45579-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45579-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="45579-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="45579-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="45579-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




