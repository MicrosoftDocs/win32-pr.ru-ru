---
description: Указывает, выполняет ли кодировщик обратную чересстрочности.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Свойство АвенквидеоинверсетелеЦининабле (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140315"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="e0328-103">АвенквидеоинверсетелеЦининабле, свойство</span><span class="sxs-lookup"><span data-stu-id="e0328-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="e0328-104">Указывает, выполняет ли кодировщик обратную чересстрочности.</span><span class="sxs-lookup"><span data-stu-id="e0328-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="e0328-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e0328-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0328-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e0328-106">Data type</span></span>

<span data-ttu-id="e0328-107">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="e0328-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e0328-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="e0328-108">Property GUID</span></span>

<span data-ttu-id="e0328-109">**КОДЕКАПИ \_ авенквидеоинверсетелеЦининабле**</span><span class="sxs-lookup"><span data-stu-id="e0328-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0328-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0328-110">Remarks</span></span>

<span data-ttu-id="e0328-111">Если значение является **вариантным \_ true**, кодировщик выполняет обратную чересстрочности.</span><span class="sxs-lookup"><span data-stu-id="e0328-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="e0328-112">Если обратный чересстрочности не требуется, задайте для этого свойства значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e0328-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="e0328-113">Чтобы выполнить инверсный чересстрочности за пределами кодировщика, присвойте этому свойству значение **Variant \_ false** и установите для свойства [**авенквидеуутпутскантипе**](avencvideooutputscantype-property.md) значение еавенквидеуутпутскан \_ самеасинпут.</span><span class="sxs-lookup"><span data-stu-id="e0328-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0328-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e0328-114">Requirements</span></span>



| <span data-ttu-id="e0328-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e0328-115">Requirement</span></span> | <span data-ttu-id="e0328-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e0328-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0328-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0328-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0328-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e0328-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e0328-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0328-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0328-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="e0328-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e0328-121">Header</span><span class="sxs-lookup"><span data-stu-id="e0328-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0328-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0328-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0328-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0328-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0328-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="e0328-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e0328-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="e0328-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




