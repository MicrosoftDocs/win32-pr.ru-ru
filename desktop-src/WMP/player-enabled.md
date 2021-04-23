---
title: Проигрыватель. включен
description: Свойство Enabled указывает или получает значение, указывающее, включен ли элемент управления проигрывателя Windows Media.
ms.assetid: 65fea4d2-3330-4cce-bdaf-fae00304271a
keywords:
- Проигрыватель Windows Media с поддержкой проигрывателя.
topic_type:
- apiref
api_name:
- Player.enabled
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d002d1f1420d17d4b1a0b7dd3028b0f2dc0f6f7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694579"
---
# <a name="playerenabled"></a><span data-ttu-id="3cb2a-104">Проигрыватель. включен</span><span class="sxs-lookup"><span data-stu-id="3cb2a-104">Player.enabled</span></span>

<span data-ttu-id="3cb2a-105">Свойство **Enabled** указывает или получает значение, указывающее, включен ли элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-105">The **enabled** property specifies or retrieves a value indicating whether the Windows Media Player control is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb2a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb2a-106">Syntax</span></span>

<span data-ttu-id="3cb2a-107">*проигрыватель* . **включено**</span><span class="sxs-lookup"><span data-stu-id="3cb2a-107">*player* .**enabled**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3cb2a-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="3cb2a-108">Possible Values</span></span>

<span data-ttu-id="3cb2a-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3cb2a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb2a-110">Value</span></span> | <span data-ttu-id="3cb2a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3cb2a-111">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="3cb2a-112">true</span><span class="sxs-lookup"><span data-stu-id="3cb2a-112">true</span></span>  | <span data-ttu-id="3cb2a-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-113">Default.</span></span> <span data-ttu-id="3cb2a-114">Элемент управления проигрывателя Windows Media включен.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-114">The Windows Media Player control is enabled.</span></span> |
| <span data-ttu-id="3cb2a-115">false</span><span class="sxs-lookup"><span data-stu-id="3cb2a-115">false</span></span> | <span data-ttu-id="3cb2a-116">Элемент управления проигрывателя Windows Media отключен.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-116">The Windows Media Player control is disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="3cb2a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cb2a-117">Remarks</span></span>

<span data-ttu-id="3cb2a-118">Если параметр **включен** имеет значение false, то во время полноэкранного воспроизведения проигрыватель Windows Media скрывает пользовательские элементы управления.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-118">If **enabled** equals false then during full-screen playback Windows Media Player hides the user controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb2a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb2a-119">Requirements</span></span>



| <span data-ttu-id="3cb2a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb2a-120">Requirement</span></span> | <span data-ttu-id="3cb2a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb2a-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb2a-122">Версия</span><span class="sxs-lookup"><span data-stu-id="3cb2a-122">Version</span></span><br/> | <span data-ttu-id="3cb2a-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3cb2a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb2a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3cb2a-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb2a-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb2a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cb2a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb2a-127">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="3cb2a-127">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





