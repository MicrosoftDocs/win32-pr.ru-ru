---
description: Включает или отключает режим формирования эскизов в видеодекодере.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Свойство Авдеквидеосумбнаилженератионмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990260"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="3d5cb-103">Авдеквидеосумбнаилженератионмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="3d5cb-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="3d5cb-104">Включает или отключает режим формирования эскизов в видеодекодере.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="3d5cb-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d5cb-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3d5cb-106">Data type</span></span>

<span data-ttu-id="3d5cb-107">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="3d5cb-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3d5cb-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="3d5cb-108">Property GUID</span></span>

<span data-ttu-id="3d5cb-109">**КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d5cb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d5cb-110">Remarks</span></span>

<span data-ttu-id="3d5cb-111">Если значение является **вариантным \_ true**, декодер использует параметр, оптимизированный для быстрого создания эскизов изображений.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="3d5cb-112">(Например, он может пропустить кадры B или P.) В противном случае, если значение является **вариантным \_ false**, декодер использует стандартные параметры декодирования.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d5cb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3d5cb-113">Requirements</span></span>



| <span data-ttu-id="3d5cb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3d5cb-114">Requirement</span></span> | <span data-ttu-id="3d5cb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3d5cb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5cb-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d5cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5cb-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d5cb-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3d5cb-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d5cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5cb-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="3d5cb-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3d5cb-120">Header</span><span class="sxs-lookup"><span data-stu-id="3d5cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5cb-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5cb-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5cb-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d5cb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5cb-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="3d5cb-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3d5cb-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




