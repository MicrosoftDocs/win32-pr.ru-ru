---
title: Network. Лостпаккетс
description: Свойство Лостпаккетс Извлекает число потерянных пакетов.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Проигрыватель Windows Media Network. Лостпаккетс
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648758"
---
# <a name="networklostpackets"></a><span data-ttu-id="36bbf-104">Network. Лостпаккетс</span><span class="sxs-lookup"><span data-stu-id="36bbf-104">Network.lostPackets</span></span>

<span data-ttu-id="36bbf-105">Свойство **лостпаккетс** Извлекает число потерянных пакетов.</span><span class="sxs-lookup"><span data-stu-id="36bbf-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bbf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36bbf-106">Syntax</span></span>

<span data-ttu-id="36bbf-107">*проигрыватель*. *сеть*. **лостпаккетс**</span><span class="sxs-lookup"><span data-stu-id="36bbf-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="36bbf-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="36bbf-108">Possible Values</span></span>

<span data-ttu-id="36bbf-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="36bbf-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="36bbf-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36bbf-110">Remarks</span></span>

<span data-ttu-id="36bbf-111">Это свойство допустимо только для потоковой передачи мультимедиа и будет равняться нулю при использовании протокола HTTP, который бездействует без потерь.</span><span class="sxs-lookup"><span data-stu-id="36bbf-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="36bbf-112">Пакеты могут быть потеряны по ряду причин, например типу и качеству сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="36bbf-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="36bbf-113">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="36bbf-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="36bbf-114">Он не сбрасывается, если воспроизведение приостановлено и перезапущено.</span><span class="sxs-lookup"><span data-stu-id="36bbf-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="36bbf-115">Это свойство возвращает действительные сведения только во время выполнения и только в случае, если *проигрыватель*. Задано свойство **URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="36bbf-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="36bbf-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="36bbf-116">Examples</span></span>

<span data-ttu-id="36bbf-117">В следующем примере JScript используется *Network*. **лостпаккетс** для вывода общего числа пакетов, потерянных во время воспроизведения, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="36bbf-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="36bbf-118">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "LP".</span><span class="sxs-lookup"><span data-stu-id="36bbf-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="36bbf-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="36bbf-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="36bbf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="36bbf-120">Requirements</span></span>



| <span data-ttu-id="36bbf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="36bbf-121">Requirement</span></span> | <span data-ttu-id="36bbf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="36bbf-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36bbf-123">Версия</span><span class="sxs-lookup"><span data-stu-id="36bbf-123">Version</span></span><br/> | <span data-ttu-id="36bbf-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="36bbf-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="36bbf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="36bbf-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="36bbf-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36bbf-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36bbf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36bbf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bbf-128">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="36bbf-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="36bbf-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="36bbf-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





