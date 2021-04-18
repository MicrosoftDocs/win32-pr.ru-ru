---
title: Внешнее событие Онколорчанже
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Онколорчанже
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Проигрыватель Windows Media для события external. Онколорчанже
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695097"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="0e6bd-105">Внешнее событие Онколорчанже</span><span class="sxs-lookup"><span data-stu-id="0e6bd-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="0e6bd-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0e6bd-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0e6bd-108">Событие **онколорчанже** возникает при изменении цвета пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="0e6bd-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0e6bd-109">Possible Values</span></span>

<span data-ttu-id="0e6bd-110">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e6bd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e6bd-111">Parameters</span></span>

<span data-ttu-id="0e6bd-112">Функция, обрабатывающая это событие, не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e6bd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e6bd-113">Remarks</span></span>

<span data-ttu-id="0e6bd-114">Пользователи могут изменять цвет пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="0e6bd-115">Это событие можно использовать для настройки внешнего вида размещенной веб-страницы в соответствии с проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="0e6bd-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6bd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0e6bd-116">Requirements</span></span>



| <span data-ttu-id="0e6bd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0e6bd-117">Requirement</span></span> | <span data-ttu-id="0e6bd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0e6bd-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6bd-119">Версия</span><span class="sxs-lookup"><span data-stu-id="0e6bd-119">Version</span></span><br/> | <span data-ttu-id="0e6bd-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0e6bd-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="0e6bd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0e6bd-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e6bd-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e6bd-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6bd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e6bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6bd-124">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="0e6bd-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





