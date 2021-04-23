---
title: Player. Виндовлессвидео
description: Свойство Виндовлессвидео указывает или получает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Проигрыватель проигрывателя Windows Media Player. Виндовлессвидео
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704336"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="7349f-104">Player. Виндовлессвидео</span><span class="sxs-lookup"><span data-stu-id="7349f-104">Player.windowlessVideo</span></span>

<span data-ttu-id="7349f-105">Свойство **виндовлессвидео** указывает или получает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.</span><span class="sxs-lookup"><span data-stu-id="7349f-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7349f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7349f-106">Syntax</span></span>

<span data-ttu-id="7349f-107">*проигрыватель*. **виндовлессвидео**</span><span class="sxs-lookup"><span data-stu-id="7349f-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7349f-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7349f-108">Possible Values</span></span>

<span data-ttu-id="7349f-109">Это **логическое** значение, заданное во время разработки и доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7349f-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="7349f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7349f-110">Value</span></span> | <span data-ttu-id="7349f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7349f-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="7349f-112">true</span><span class="sxs-lookup"><span data-stu-id="7349f-112">true</span></span>  | <span data-ttu-id="7349f-113">Видео отображается в режиме без окон.</span><span class="sxs-lookup"><span data-stu-id="7349f-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="7349f-114">false</span><span class="sxs-lookup"><span data-stu-id="7349f-114">false</span></span> | <span data-ttu-id="7349f-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7349f-115">Default.</span></span> <span data-ttu-id="7349f-116">Видео отображается в режиме с окнами.</span><span class="sxs-lookup"><span data-stu-id="7349f-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7349f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7349f-117">Remarks</span></span>

<span data-ttu-id="7349f-118">По умолчанию встроенный элемент управления проигрывателя Windows Media визуализирует видео в отдельном окне в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="7349f-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="7349f-119">Если для **виндовлессвидео** задано значение true, элемент управления проигрывателя визуализирует видео непосредственно в клиентской области, поэтому можно применять специальные эффекты или разносить видео с текстом.</span><span class="sxs-lookup"><span data-stu-id="7349f-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="7349f-120">В Windows Vista отрисовка видео в режиме без окон может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="7349f-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="7349f-121">Свойство **виндовлессвидео** не поддерживается для Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="7349f-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="7349f-122">Установка значения этого свойства в навигаторе может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="7349f-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="7349f-123">**Проигрыватель Windows Media 10 Mobile:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7349f-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7349f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7349f-124">Requirements</span></span>



| <span data-ttu-id="7349f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7349f-125">Requirement</span></span> | <span data-ttu-id="7349f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7349f-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7349f-127">Версия</span><span class="sxs-lookup"><span data-stu-id="7349f-127">Version</span></span><br/> | <span data-ttu-id="7349f-128">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7349f-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="7349f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7349f-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7349f-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7349f-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





