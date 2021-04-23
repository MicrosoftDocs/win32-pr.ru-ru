---
title: Settings. Инвокеурлс
description: Свойство Инвокеурлс указывает или получает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Проигрыватель Windows Media Settings. Инвокеурлс
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648668"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="0d103-104">Settings. Инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="0d103-104">Settings.invokeURLs</span></span>

<span data-ttu-id="0d103-105">Свойство **инвокеурлс** указывает или получает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="0d103-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d103-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d103-106">Syntax</span></span>

<span data-ttu-id="0d103-107">Player. Settings. Инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="0d103-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="0d103-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0d103-108">Possible Values</span></span>

<span data-ttu-id="0d103-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0d103-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0d103-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0d103-110">Value</span></span> | <span data-ttu-id="0d103-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0d103-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="0d103-112">true</span><span class="sxs-lookup"><span data-stu-id="0d103-112">true</span></span>  | <span data-ttu-id="0d103-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d103-113">Default.</span></span> <span data-ttu-id="0d103-114">События URL-адреса должны запускать браузер.</span><span class="sxs-lookup"><span data-stu-id="0d103-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="0d103-115">false</span><span class="sxs-lookup"><span data-stu-id="0d103-115">false</span></span> | <span data-ttu-id="0d103-116">События URL-адреса не должны запускать браузер.</span><span class="sxs-lookup"><span data-stu-id="0d103-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="0d103-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d103-117">Remarks</span></span>

<span data-ttu-id="0d103-118">Файлы мультимедиа могут содержать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="0d103-118">Media files can contain URLs.</span></span> <span data-ttu-id="0d103-119">При отправке URL-адреса элементу управления проигрывателя Windows Media он сначала передается обработчику событий **команду скрипта** независимо от значения в **инвокеурлс**.</span><span class="sxs-lookup"><span data-stu-id="0d103-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="0d103-120">После выхода из **команду скрипта** проигрыватель Windows Media проверяет **инвокеурлс** , чтобы определить, следует ли запускать браузер по умолчанию с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="0d103-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="0d103-121">Вы можете выборочно отображать URL-адреса, проверив их в **команду скрипта** и установив нужные **инвокеурлс** .</span><span class="sxs-lookup"><span data-stu-id="0d103-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="0d103-122">**Проигрыватель Windows Media 10 Mobile**: это свойство принимает или возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="0d103-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d103-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0d103-123">Requirements</span></span>



| <span data-ttu-id="0d103-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0d103-124">Requirement</span></span> | <span data-ttu-id="0d103-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0d103-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d103-126">Версия</span><span class="sxs-lookup"><span data-stu-id="0d103-126">Version</span></span><br/> | <span data-ttu-id="0d103-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0d103-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0d103-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0d103-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d103-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d103-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d103-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d103-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d103-131">**Событие Player. команду скрипта**</span><span class="sxs-lookup"><span data-stu-id="0d103-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="0d103-132">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="0d103-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





