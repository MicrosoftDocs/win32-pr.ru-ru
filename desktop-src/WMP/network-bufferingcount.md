---
title: Network. Буфферингкаунт
description: Свойство Буфферингкаунт извлекает количество попыток буферизации во время воспроизведения клипа.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Проигрыватель Windows Media Network. Буфферингкаунт
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704218"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="699bd-104">Network. Буфферингкаунт</span><span class="sxs-lookup"><span data-stu-id="699bd-104">Network.bufferingCount</span></span>

<span data-ttu-id="699bd-105">Свойство **буфферингкаунт** извлекает количество попыток буферизации во время воспроизведения клипа.</span><span class="sxs-lookup"><span data-stu-id="699bd-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="699bd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="699bd-106">Syntax</span></span>

<span data-ttu-id="699bd-107">*проигрыватель*. *сеть*. **буфферингкаунт**</span><span class="sxs-lookup"><span data-stu-id="699bd-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="699bd-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="699bd-108">Possible Values</span></span>

<span data-ttu-id="699bd-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="699bd-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="699bd-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="699bd-110">Remarks</span></span>

<span data-ttu-id="699bd-111">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="699bd-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="699bd-112">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="699bd-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="699bd-113">Буферизация применяется только к потоковой передаче содержимого.</span><span class="sxs-lookup"><span data-stu-id="699bd-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="699bd-114">Это свойство возвращает действительные сведения только во время выполнения, когда *проигрыватель*. Задано свойство **URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="699bd-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="699bd-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="699bd-115">Examples</span></span>

<span data-ttu-id="699bd-116">В следующем примере JScript используется *Network*. **буфферингкаунт** для вывода количества попыток буферизации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="699bd-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="699bd-117">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "CB".</span><span class="sxs-lookup"><span data-stu-id="699bd-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="699bd-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="699bd-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="699bd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="699bd-119">Requirements</span></span>



| <span data-ttu-id="699bd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="699bd-120">Requirement</span></span> | <span data-ttu-id="699bd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="699bd-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="699bd-122">Версия</span><span class="sxs-lookup"><span data-stu-id="699bd-122">Version</span></span><br/> | <span data-ttu-id="699bd-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="699bd-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="699bd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="699bd-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="699bd-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="699bd-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="699bd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="699bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699bd-127">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="699bd-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="699bd-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="699bd-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





