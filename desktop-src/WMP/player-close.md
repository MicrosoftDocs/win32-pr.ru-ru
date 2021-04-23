---
title: Метод Player. Close
description: Метод Close освобождает ресурсы проигрывателя Windows Media.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- закрыть метод проигрыватель Windows Media Player
- закрыть метод проигрыватель Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695186"
---
# <a name="playerclose-method"></a><span data-ttu-id="b0df9-106">Метод Player. Close</span><span class="sxs-lookup"><span data-stu-id="b0df9-106">Player.close method</span></span>

<span data-ttu-id="b0df9-107">Метод **Close** освобождает ресурсы проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b0df9-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0df9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0df9-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="b0df9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0df9-109">Parameters</span></span>

<span data-ttu-id="b0df9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b0df9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0df9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0df9-111">Return value</span></span>

<span data-ttu-id="b0df9-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b0df9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0df9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0df9-113">Remarks</span></span>

<span data-ttu-id="b0df9-114">Этот метод закрывает текущий файл мультимедиа, а не проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b0df9-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="b0df9-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="b0df9-115">Examples</span></span>

<span data-ttu-id="b0df9-116">В следующем примере создается HTML-элемент BUTTON, который при щелчке останавливает воспроизведение в проигрывателе Windows Media и освобождает используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b0df9-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="b0df9-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="b0df9-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="b0df9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b0df9-118">Requirements</span></span>



| <span data-ttu-id="b0df9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b0df9-119">Requirement</span></span> | <span data-ttu-id="b0df9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b0df9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0df9-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b0df9-121">Version</span></span><br/> | <span data-ttu-id="b0df9-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b0df9-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b0df9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b0df9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0df9-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0df9-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0df9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0df9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0df9-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="b0df9-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





