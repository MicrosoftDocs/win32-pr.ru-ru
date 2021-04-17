---
title: Player. Стретчтофит
description: Свойство Стретчтофит указывает или получает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Проигрыватель проигрывателя Windows Media Player. Стретчтофит
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704150"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="0da59-104">Player. Стретчтофит</span><span class="sxs-lookup"><span data-stu-id="0da59-104">Player.stretchToFit</span></span>

<span data-ttu-id="0da59-105">Свойство **стретчтофит** указывает или получает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.</span><span class="sxs-lookup"><span data-stu-id="0da59-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da59-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0da59-106">Syntax</span></span>

<span data-ttu-id="0da59-107">*проигрыватель*. **стретчтофит**</span><span class="sxs-lookup"><span data-stu-id="0da59-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0da59-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0da59-108">Possible Values</span></span>

<span data-ttu-id="0da59-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0da59-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0da59-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0da59-110">Value</span></span> | <span data-ttu-id="0da59-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0da59-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="0da59-112">true</span><span class="sxs-lookup"><span data-stu-id="0da59-112">true</span></span>  | <span data-ttu-id="0da59-113">Видео будет растягиваться по размеру окна.</span><span class="sxs-lookup"><span data-stu-id="0da59-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="0da59-114">false</span><span class="sxs-lookup"><span data-stu-id="0da59-114">false</span></span> | <span data-ttu-id="0da59-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0da59-115">Default.</span></span> <span data-ttu-id="0da59-116">Видео не будет растягиваться по размеру окна.</span><span class="sxs-lookup"><span data-stu-id="0da59-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0da59-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0da59-117">Remarks</span></span>

<span data-ttu-id="0da59-118">Если **стретчтофит** имеет значение true, элемент управления проигрывателя Windows Media сохраняет исходные пропорции видео.</span><span class="sxs-lookup"><span data-stu-id="0da59-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="0da59-119">Если пропорции видео не соответствуют пропорциям видеоокна, то области с черной маской могут отображаться в верхней и нижней, левой и правой частях изображения видео.</span><span class="sxs-lookup"><span data-stu-id="0da59-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="0da59-120">Это свойство применяется к элементу управления проигрывателя Windows Media только при внедрении в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="0da59-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="0da59-121">**Проигрыватель Windows Media 10 Mobile:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0da59-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da59-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0da59-122">Requirements</span></span>



| <span data-ttu-id="0da59-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0da59-123">Requirement</span></span> | <span data-ttu-id="0da59-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0da59-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0da59-125">Версия</span><span class="sxs-lookup"><span data-stu-id="0da59-125">Version</span></span><br/> | <span data-ttu-id="0da59-126">Проигрыватель Windows Media версии 7,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0da59-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="0da59-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0da59-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="0da59-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0da59-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da59-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0da59-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da59-130">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="0da59-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





