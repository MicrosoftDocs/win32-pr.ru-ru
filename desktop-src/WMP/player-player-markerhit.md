---
title: Событие Player. Маркерхит
description: Событие Маркерхит возникает при достижении маркера. | Событие Player. Маркерхит
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Проигрыватель Windows Media Event Маркерхит
- Проигрыватель Windows Media Event Маркерхит, класс Player
- Класс проигрывателя Windows Media Player, событие Маркерхит
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685300"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="45f6d-107">Событие Player. Маркерхит</span><span class="sxs-lookup"><span data-stu-id="45f6d-107">Player.MarkerHit event</span></span>

<span data-ttu-id="45f6d-108">Событие **маркерхит** возникает при достижении маркера.</span><span class="sxs-lookup"><span data-stu-id="45f6d-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f6d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45f6d-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="45f6d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f6d-111">*маркернум*</span><span class="sxs-lookup"><span data-stu-id="45f6d-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="45f6d-112">**Число** (**длинное**), указывающее число попаданий маркера.</span><span class="sxs-lookup"><span data-stu-id="45f6d-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f6d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45f6d-113">Return value</span></span>

<span data-ttu-id="45f6d-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="45f6d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f6d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45f6d-115">Remarks</span></span>

<span data-ttu-id="45f6d-116">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="45f6d-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="45f6d-117">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="45f6d-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f6d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="45f6d-118">Requirements</span></span>



| <span data-ttu-id="45f6d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="45f6d-119">Requirement</span></span> | <span data-ttu-id="45f6d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="45f6d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45f6d-121">Версия</span><span class="sxs-lookup"><span data-stu-id="45f6d-121">Version</span></span><br/> | <span data-ttu-id="45f6d-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="45f6d-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="45f6d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="45f6d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="45f6d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45f6d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f6d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45f6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f6d-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="45f6d-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





