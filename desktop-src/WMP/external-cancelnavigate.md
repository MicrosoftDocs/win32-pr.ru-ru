---
title: External. Канцелнавигате, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Канцелнавигате, метод
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Канцелнавигате метод Windows Media Player
- Канцелнавигате метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Канцелнавигате
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698892"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="7ff67-107">External. Канцелнавигате, метод</span><span class="sxs-lookup"><span data-stu-id="7ff67-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="7ff67-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="7ff67-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7ff67-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7ff67-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7ff67-110">Метод **канцелнавигате** информирует проигрыватель Windows Media, что он не должен отображать новую страницу обнаружения, даже если представление изменилось в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="7ff67-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff67-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ff67-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="7ff67-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ff67-112">Parameters</span></span>

<span data-ttu-id="7ff67-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7ff67-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ff67-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ff67-114">Return value</span></span>

<span data-ttu-id="7ff67-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ff67-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff67-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ff67-116">Remarks</span></span>

<span data-ttu-id="7ff67-117">Когда представление изменяется в проигрывателе Windows Media Player, проигрыватель вызывает подключаемый модуль интернет-магазина, чтобы определить, какая страница обнаружения должна отображаться далее.</span><span class="sxs-lookup"><span data-stu-id="7ff67-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="7ff67-118">Однако в некоторых случаях в Интернет-магазине может потребоваться, чтобы проигрыватель продолжал отображать существующую страницу обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7ff67-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="7ff67-119">Следующая процедура определяет, отображается ли в проигрывателе новая страница обнаружения:</span><span class="sxs-lookup"><span data-stu-id="7ff67-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="7ff67-120">Действие, выполняемое пользователем либо в пользовательском интерфейсе проигрывателя, либо на странице Обнаружение, запрашивает изменение его представления проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="7ff67-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="7ff67-121">Проигрыватель вызывает метод метода- [шаблона](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) подключаемого модуля, чтобы определить, какая страница обнаружения должна отображаться далее.</span><span class="sxs-lookup"><span data-stu-id="7ff67-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="7ff67-122">Проигрыватель сохраняет URL-адрес новой страницы обнаружения, но в данный момент не отображает новую страницу обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7ff67-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="7ff67-123">Проигрыватель создает событие [онвиевчанже](external-onviewchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff67-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="7ff67-124">Если обработчик событий **онвиевчанже** на странице обнаружения вызывает **канцелнавигате**, проигрыватель не отображает новую страницу обнаружения (определенную на шаге 2).</span><span class="sxs-lookup"><span data-stu-id="7ff67-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="7ff67-125">Вместо этого будет отображаться существующая страница обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7ff67-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="7ff67-126">Если обработчик событий **онвиевчанже** не вызывает **канцелнавигате**, игрок отображает новую страницу обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7ff67-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="7ff67-127">Например, предположим, что в настоящий момент в проигрывателе отображается представление альбома, для которого выбрана определенная запись.</span><span class="sxs-lookup"><span data-stu-id="7ff67-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="7ff67-128">Также предположим, что текущая страница обнаружения — это страница, представляющая весь альбом.</span><span class="sxs-lookup"><span data-stu-id="7ff67-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="7ff67-129">Если пользователь щелкает другую запись из того же альбома, вид проигрывателя немного меняется, чтобы показать, что выбрана новая запись.</span><span class="sxs-lookup"><span data-stu-id="7ff67-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="7ff67-130">Но нет необходимости отображать новую страницу обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7ff67-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="7ff67-131">Страница обнаружения, представляющая весь альбом, по-прежнему является соответствующей страницей для проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="7ff67-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff67-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7ff67-132">Requirements</span></span>



| <span data-ttu-id="7ff67-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7ff67-133">Requirement</span></span> | <span data-ttu-id="7ff67-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7ff67-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff67-135">Версия</span><span class="sxs-lookup"><span data-stu-id="7ff67-135">Version</span></span><br/> | <span data-ttu-id="7ff67-136">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="7ff67-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="7ff67-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff67-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="7ff67-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff67-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff67-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ff67-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff67-140">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="7ff67-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7ff67-141">**External. Чанжевиевонлинелист**</span><span class="sxs-lookup"><span data-stu-id="7ff67-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="7ff67-142">**External. Онвиевчанже**</span><span class="sxs-lookup"><span data-stu-id="7ff67-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





