---
title: Внешнее событие Ончанжевиеверрор
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Ончанжевиеверрор
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Проигрыватель Windows Media для события external. Ончанжевиеверрор
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698885"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="c7508-105">Внешнее событие Ончанжевиеверрор</span><span class="sxs-lookup"><span data-stu-id="c7508-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="c7508-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="c7508-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c7508-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7508-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c7508-108">Событие **ончанжевиеверрор** возникает, когда вызов метода [External. чанжевиев](external-changeview.md) приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c7508-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="c7508-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c7508-109">Possible Values</span></span>

<span data-ttu-id="c7508-110">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="c7508-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7508-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7508-111">Parameters</span></span>

<span data-ttu-id="c7508-112">Функция, обрабатывающая это событие, имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="c7508-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="c7508-113"><span id="hr"></span><span id="HR"></span>*кадров*</span><span class="sxs-lookup"><span data-stu-id="c7508-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="c7508-114">Код ошибки **HRESULT** , указывающий причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="c7508-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="c7508-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*либрарилокатионтипе*</span><span class="sxs-lookup"><span data-stu-id="c7508-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="c7508-116">Та же строка, которая была передана в параметре **либрарилокатионтипе** объекта **чанжевиев**.</span><span class="sxs-lookup"><span data-stu-id="c7508-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="c7508-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*либрарилокатионид*</span><span class="sxs-lookup"><span data-stu-id="c7508-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="c7508-118">Строка сатвас, переданная в параметре **либрарилокатионид** объекта **чанжевиев**.</span><span class="sxs-lookup"><span data-stu-id="c7508-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="c7508-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Фильтрация*</span><span class="sxs-lookup"><span data-stu-id="c7508-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="c7508-120">Та же строка, которая была передана в параметре **Filter** параметра **чанжевиев**.</span><span class="sxs-lookup"><span data-stu-id="c7508-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="c7508-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*виевпарамс*</span><span class="sxs-lookup"><span data-stu-id="c7508-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="c7508-122">Та же строка, которая была передана в параметре **виевпарамс** объекта **чанжевиев**.</span><span class="sxs-lookup"><span data-stu-id="c7508-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7508-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c7508-123">Requirements</span></span>



| <span data-ttu-id="c7508-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c7508-124">Requirement</span></span> | <span data-ttu-id="c7508-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c7508-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7508-126">Версия</span><span class="sxs-lookup"><span data-stu-id="c7508-126">Version</span></span><br/> | <span data-ttu-id="c7508-127">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c7508-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="c7508-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c7508-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7508-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7508-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7508-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7508-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7508-131">**Екстерналобжект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="c7508-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





