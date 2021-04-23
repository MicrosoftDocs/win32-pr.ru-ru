---
title: Network. частота
description: Свойство частота кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд. Например, значение 2998 означает 29,98 кадров в секунду.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Проигрыватель Windows Media Network. частоты кадров
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708324"
---
# <a name="networkframerate"></a><span data-ttu-id="0d9b7-105">Network. частота</span><span class="sxs-lookup"><span data-stu-id="0d9b7-105">Network.frameRate</span></span>

<span data-ttu-id="0d9b7-106">Свойство **Частота** кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд.</span><span class="sxs-lookup"><span data-stu-id="0d9b7-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="0d9b7-107">Например, значение 2998 означает 29,98 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="0d9b7-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d9b7-108">Syntax</span></span>

<span data-ttu-id="0d9b7-109">*проигрыватель*. *сеть*. **Частота кадров**</span><span class="sxs-lookup"><span data-stu-id="0d9b7-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0d9b7-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0d9b7-110">Possible Values</span></span>

<span data-ttu-id="0d9b7-111">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="0d9b7-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="0d9b7-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d9b7-112">Examples</span></span>

<span data-ttu-id="0d9b7-113">В следующем примере JScript используется *Network*. **Частота кадров для вывода** текущей частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="0d9b7-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="0d9b7-114">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="0d9b7-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="0d9b7-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="0d9b7-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="0d9b7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0d9b7-116">Requirements</span></span>



| <span data-ttu-id="0d9b7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0d9b7-117">Requirement</span></span> | <span data-ttu-id="0d9b7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0d9b7-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9b7-119">Версия</span><span class="sxs-lookup"><span data-stu-id="0d9b7-119">Version</span></span><br/> | <span data-ttu-id="0d9b7-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0d9b7-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0d9b7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9b7-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d9b7-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d9b7-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d9b7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d9b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9b7-124">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="0d9b7-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="0d9b7-125">**Network. Енкодедфрамерате**</span><span class="sxs-lookup"><span data-stu-id="0d9b7-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





