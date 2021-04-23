---
title: Внешнее событие Ончанжевиевонлинелистеррор
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Ончанжевиевонлинелистеррор
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Проигрыватель Windows Media для события external. Ончанжевиевонлинелистеррор
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698884"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="7c61c-105">Внешнее событие Ончанжевиевонлинелистеррор</span><span class="sxs-lookup"><span data-stu-id="7c61c-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="7c61c-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="7c61c-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7c61c-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c61c-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7c61c-108">Событие **ончанжевиевонлинелистеррор** возникает, когда вызов метода [External. чанжевиевонлинелист](external-changeviewonlinelist.md) приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="7c61c-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="7c61c-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7c61c-109">Possible Values</span></span>

<span data-ttu-id="7c61c-110">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="7c61c-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c61c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c61c-111">Parameters</span></span>

<span data-ttu-id="7c61c-112">Функция, обрабатывающая эту ошибку, имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="7c61c-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="7c61c-113"><span id="hr"></span><span id="HR"></span>*кадров*</span><span class="sxs-lookup"><span data-stu-id="7c61c-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-114">Код ошибки **HRESULT** , указывающий причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="7c61c-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*либрарилокатионтипе*</span><span class="sxs-lookup"><span data-stu-id="7c61c-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-116">Та же строка, которая была передана в параметре **либрарилокатионтипе** объекта **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*либрарилокатионид*</span><span class="sxs-lookup"><span data-stu-id="7c61c-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-118">Та же строка, которая была передана в параметре **либрарилокатионид** объекта **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="7c61c-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-120">Та же строка, которая была передана в параметре **params** объекта **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="7c61c-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-122">Та же строка, которая была передана в параметре **FriendlyName** параметра **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*листтипе*</span><span class="sxs-lookup"><span data-stu-id="7c61c-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-124">Та же строка, которая была передана в параметре **листтипе** объекта **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="7c61c-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-126">Та же строка, которая была передана в параметре **ViewMode** объекта **чанжевиевонлинелист**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c61c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7c61c-127">Requirements</span></span>



| <span data-ttu-id="7c61c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7c61c-128">Requirement</span></span> | <span data-ttu-id="7c61c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7c61c-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c61c-130">Версия</span><span class="sxs-lookup"><span data-stu-id="7c61c-130">Version</span></span><br/> | <span data-ttu-id="7c61c-131">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7c61c-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7c61c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7c61c-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c61c-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c61c-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c61c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c61c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c61c-135">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="7c61c-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





