---
title: Network. Фрамесскиппед
description: Свойство Фрамесскиппед извлекает общее число кадров, пропущенных во время воспроизведения.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Проигрыватель Windows Media Network. Фрамесскиппед
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708323"
---
# <a name="networkframesskipped"></a><span data-ttu-id="803e7-104">Network. Фрамесскиппед</span><span class="sxs-lookup"><span data-stu-id="803e7-104">Network.framesSkipped</span></span>

<span data-ttu-id="803e7-105">Свойство **фрамесскиппед** извлекает общее число кадров, пропущенных во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="803e7-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="803e7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="803e7-106">Syntax</span></span>

<span data-ttu-id="803e7-107">*проигрыватель*. *сеть*. **фрамесскиппед**</span><span class="sxs-lookup"><span data-stu-id="803e7-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="803e7-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="803e7-108">Possible Values</span></span>

<span data-ttu-id="803e7-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="803e7-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="803e7-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="803e7-110">Examples</span></span>

<span data-ttu-id="803e7-111">В следующем примере JScript используется *Network*. **фрамесскиппед** для вывода общего числа кадров, пропущенных во время воспроизведения, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="803e7-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="803e7-112">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FS".</span><span class="sxs-lookup"><span data-stu-id="803e7-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="803e7-113">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="803e7-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="803e7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="803e7-114">Requirements</span></span>



| <span data-ttu-id="803e7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="803e7-115">Requirement</span></span> | <span data-ttu-id="803e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="803e7-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="803e7-117">Версия</span><span class="sxs-lookup"><span data-stu-id="803e7-117">Version</span></span><br/> | <span data-ttu-id="803e7-118">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="803e7-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="803e7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="803e7-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="803e7-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803e7-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803e7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="803e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803e7-122">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="803e7-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





