---
title: Network. Енкодедфрамерате
description: Свойство Енкодедфрамерате извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Проигрыватель Windows Media Network. Енкодедфрамерате
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708365"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="6b993-104">Network. Енкодедфрамерате</span><span class="sxs-lookup"><span data-stu-id="6b993-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="6b993-105">Свойство **енкодедфрамерате** извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="6b993-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b993-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b993-106">Syntax</span></span>

<span data-ttu-id="6b993-107">*проигрыватель*. *сеть*. **енкодедфрамерате**</span><span class="sxs-lookup"><span data-stu-id="6b993-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6b993-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6b993-108">Possible Values</span></span>

<span data-ttu-id="6b993-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="6b993-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="6b993-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="6b993-110">Examples</span></span>

<span data-ttu-id="6b993-111">В следующем примере JScript используется *Network*. **енкодедфрамерате** для вывода частоты кадров, указанной при кодировании файла.</span><span class="sxs-lookup"><span data-stu-id="6b993-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="6b993-112">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="6b993-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="6b993-113">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="6b993-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6b993-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6b993-114">Requirements</span></span>



| <span data-ttu-id="6b993-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6b993-115">Requirement</span></span> | <span data-ttu-id="6b993-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6b993-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b993-117">Версия</span><span class="sxs-lookup"><span data-stu-id="6b993-117">Version</span></span><br/> | <span data-ttu-id="6b993-118">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6b993-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b993-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6b993-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b993-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b993-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b993-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b993-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b993-122">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="6b993-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="6b993-123">**Network. частота**</span><span class="sxs-lookup"><span data-stu-id="6b993-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





