---
title: Внешнее событие Онвиевчанже
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Событие Онвиевчанже возникает при изменении представления в проигрывателе Windows Media.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Проигрыватель Windows Media для события external. Онвиевчанже
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694492"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="836de-106">Внешнее событие Онвиевчанже</span><span class="sxs-lookup"><span data-stu-id="836de-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="836de-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="836de-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="836de-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="836de-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="836de-109">Событие **онвиевчанже** возникает при изменении представления в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="836de-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="836de-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="836de-110">Possible Values</span></span>

<span data-ttu-id="836de-111">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="836de-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="836de-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="836de-112">Parameters</span></span>

<span data-ttu-id="836de-113">Функция, обрабатывающая это событие, не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="836de-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="836de-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="836de-114">Remarks</span></span>

<span data-ttu-id="836de-115">Представление в проигрывателе Windows Media может измениться по любой из следующих причин.</span><span class="sxs-lookup"><span data-stu-id="836de-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="836de-116">Пользователь взаимодействует с пользовательским интерфейсом проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="836de-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="836de-117">Пользователь взаимодействует со страницей обнаружения, а скрипт на странице обнаружения вызывает [External. чанжевиев](external-changeview.md).</span><span class="sxs-lookup"><span data-stu-id="836de-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="836de-118">Пользователь взаимодействует со страницей обнаружения, а скрипт на странице обнаружения вызывает [External. чанжевиевонлинелист](external-changeviewonlinelist.md).</span><span class="sxs-lookup"><span data-stu-id="836de-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="836de-119">При изменении представления в проигрывателе Windows Media проигрыватель вызывает [ивмпконтентпартнер::-Template](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , чтобы получить отображаемый URL-адрес следующей страницы обнаружения.</span><span class="sxs-lookup"><span data-stu-id="836de-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="836de-120">Однако до того, как проигрыватель отобразит новую страницу обнаружения, он вызывает событие **онвиевчанже** .</span><span class="sxs-lookup"><span data-stu-id="836de-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="836de-121">Если обработчик событий **онвиевчанже** вызывает [External. канцелнавигате](external-cancelnavigate.md), проигрыватель Windows Media не отображает новую страницу обнаружения.</span><span class="sxs-lookup"><span data-stu-id="836de-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="836de-122">Вместо этого будет отображаться текущая страница обнаружения.</span><span class="sxs-lookup"><span data-stu-id="836de-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="836de-123">Требования</span><span class="sxs-lookup"><span data-stu-id="836de-123">Requirements</span></span>



| <span data-ttu-id="836de-124">Требование</span><span class="sxs-lookup"><span data-stu-id="836de-124">Requirement</span></span> | <span data-ttu-id="836de-125">Значение</span><span class="sxs-lookup"><span data-stu-id="836de-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="836de-126">Версия</span><span class="sxs-lookup"><span data-stu-id="836de-126">Version</span></span><br/> | <span data-ttu-id="836de-127">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="836de-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="836de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="836de-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="836de-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="836de-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836de-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="836de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836de-131">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="836de-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="836de-132">**External. Чанжевиев**</span><span class="sxs-lookup"><span data-stu-id="836de-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="836de-133">**External. Чанжевиевонлинелист**</span><span class="sxs-lookup"><span data-stu-id="836de-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





