---
title: Network. скорость
description: Свойство скорость получает текущую скорость получения.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Проигрыватель Windows Media с сетевым. скоростью
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704220"
---
# <a name="networkbitrate"></a><span data-ttu-id="ed31e-104">Network. скорость</span><span class="sxs-lookup"><span data-stu-id="ed31e-104">Network.bitRate</span></span>

<span data-ttu-id="ed31e-105">Свойство **скорость** получает текущую скорость получения.</span><span class="sxs-lookup"><span data-stu-id="ed31e-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed31e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed31e-106">Syntax</span></span>

<span data-ttu-id="ed31e-107">*проигрыватель*. *сеть*. **скорость**</span><span class="sxs-lookup"><span data-stu-id="ed31e-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ed31e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ed31e-108">Possible Values</span></span>

<span data-ttu-id="ed31e-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="ed31e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed31e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed31e-110">Remarks</span></span>

<span data-ttu-id="ed31e-111">Это значение представляет собой сочетание скорости потока для текущих видео-и звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="ed31e-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="ed31e-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed31e-112">Examples</span></span>

<span data-ttu-id="ed31e-113">В следующем примере JScript используется *Network*. **скорость** для вывода скорости текущего мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed31e-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="ed31e-114">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BR".</span><span class="sxs-lookup"><span data-stu-id="ed31e-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="ed31e-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="ed31e-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="ed31e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ed31e-116">Requirements</span></span>



| <span data-ttu-id="ed31e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ed31e-117">Requirement</span></span> | <span data-ttu-id="ed31e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ed31e-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed31e-119">Версия</span><span class="sxs-lookup"><span data-stu-id="ed31e-119">Version</span></span><br/> | <span data-ttu-id="ed31e-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ed31e-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ed31e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ed31e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed31e-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed31e-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed31e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed31e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed31e-124">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="ed31e-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





