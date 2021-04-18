---
title: Network. Саурцепротокол
description: Свойство Саурцепротокол получает исходный протокол, используемый для получения данных.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Проигрыватель Windows Media Network. Саурцепротокол
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694816"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="b3465-104">Network. Саурцепротокол</span><span class="sxs-lookup"><span data-stu-id="b3465-104">Network.sourceProtocol</span></span>

<span data-ttu-id="b3465-105">Свойство **саурцепротокол** получает исходный протокол, используемый для получения данных.</span><span class="sxs-lookup"><span data-stu-id="b3465-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3465-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3465-106">Syntax</span></span>

<span data-ttu-id="b3465-107">*проигрыватель*. *сеть*. **саурцепротокол**</span><span class="sxs-lookup"><span data-stu-id="b3465-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b3465-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b3465-108">Possible Values</span></span>

<span data-ttu-id="b3465-109">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b3465-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3465-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3465-110">Remarks</span></span>

<span data-ttu-id="b3465-111">Это свойство имеет значение "" (пустая строка) при воспроизведении мультимедиа с компакт-диска или DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="b3465-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="b3465-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="b3465-112">Examples</span></span>

<span data-ttu-id="b3465-113">В следующем примере JScript используется *Network*. **саурцепротокол** для вывода исходного протокола, используемого для получения данных.</span><span class="sxs-lookup"><span data-stu-id="b3465-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="b3465-114">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "SP".</span><span class="sxs-lookup"><span data-stu-id="b3465-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="b3465-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="b3465-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="b3465-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b3465-116">Requirements</span></span>



| <span data-ttu-id="b3465-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b3465-117">Requirement</span></span> | <span data-ttu-id="b3465-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b3465-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3465-119">Версия</span><span class="sxs-lookup"><span data-stu-id="b3465-119">Version</span></span><br/> | <span data-ttu-id="b3465-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b3465-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3465-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b3465-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3465-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3465-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3465-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3465-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3465-124">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="b3465-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





