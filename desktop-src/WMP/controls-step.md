---
title: Метод Controls. Step
description: Метод Step заставляет текущий видеоматериал закреплять воспроизведение на следующем кадре или предыдущем кадре.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Пошаговый метод проигрывателя Windows Media
- Пошаговый метод Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694943"
---
# <a name="controlsstep-method"></a><span data-ttu-id="efb59-106">Метод Controls. Step</span><span class="sxs-lookup"><span data-stu-id="efb59-106">Controls.step method</span></span>

<span data-ttu-id="efb59-107">Метод **Step** заставляет текущий видеоматериал закреплять воспроизведение на следующем кадре или предыдущем кадре.</span><span class="sxs-lookup"><span data-stu-id="efb59-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb59-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efb59-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="efb59-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="efb59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb59-110">*фрамекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efb59-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb59-111">**Число** (**длинное**), указывающее, сколько кадров следует пошагово перед замораживанием.</span><span class="sxs-lookup"><span data-stu-id="efb59-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="efb59-112">В настоящее время необходимо задать значение 1 или-1.</span><span class="sxs-lookup"><span data-stu-id="efb59-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb59-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efb59-113">Return value</span></span>

<span data-ttu-id="efb59-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="efb59-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb59-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efb59-115">Remarks</span></span>

<span data-ttu-id="efb59-116">В настоящее время этот метод поддерживает только параметры 1 или-1, поэтому каждый раз можно пошаговым образом выполнять только один кадр.</span><span class="sxs-lookup"><span data-stu-id="efb59-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="efb59-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="efb59-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb59-118">Требования</span><span class="sxs-lookup"><span data-stu-id="efb59-118">Requirements</span></span>



| <span data-ttu-id="efb59-119">Требование</span><span class="sxs-lookup"><span data-stu-id="efb59-119">Requirement</span></span> | <span data-ttu-id="efb59-120">Значение</span><span class="sxs-lookup"><span data-stu-id="efb59-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="efb59-121">Версия</span><span class="sxs-lookup"><span data-stu-id="efb59-121">Version</span></span><br/> | <span data-ttu-id="efb59-122">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="efb59-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="efb59-123">DLL</span><span class="sxs-lookup"><span data-stu-id="efb59-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="efb59-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb59-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb59-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efb59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb59-126">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="efb59-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="efb59-127">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="efb59-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





