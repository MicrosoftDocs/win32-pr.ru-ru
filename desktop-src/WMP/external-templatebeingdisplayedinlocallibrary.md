---
title: External. Темплатебеингдисплайединлокаллибрари
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Темплатебеингдисплайединлокаллибрари
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Внешний Темплатебеингдисплайединлокаллибрари проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695060"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="a3af1-105">External. Темплатебеингдисплайединлокаллибрари</span><span class="sxs-lookup"><span data-stu-id="a3af1-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="a3af1-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="a3af1-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a3af1-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a3af1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a3af1-108">Свойство **темплатебеингдисплайединлокаллибрари** указывает, отображается ли веб-канал, представленный текущей страницей обнаружения, в элементе управления представления дерева локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="a3af1-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3af1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3af1-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="a3af1-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a3af1-110">Possible Values</span></span>

<span data-ttu-id="a3af1-111">Это свойство является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a3af1-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="a3af1-112">**Значение true** указывает, что веб-канал отображается в дереве локальной библиотеки — элемент управления View.</span><span class="sxs-lookup"><span data-stu-id="a3af1-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3af1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3af1-113">Remarks</span></span>

<span data-ttu-id="a3af1-114">Страница обнаружения, представляющая канал для динамического списка воспроизведения, может отображать кнопку, позволяющую пользователю сохранить веб-канал в своей локальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a3af1-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="a3af1-115">Сохранение канала в этом контексте означает, что некоторые метаданные сохраняются на компьютере пользователя, а веб-канал отображается в узле **списки воспроизведения** в дереве локальной библиотеки — элемент управления View.</span><span class="sxs-lookup"><span data-stu-id="a3af1-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="a3af1-116">Скрипт на странице обнаружения может проверить свойство **темплатебеингдисплайединлокаллибрари** , чтобы определить, сохранил ли пользователь веб-канал в локальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a3af1-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="a3af1-117">Если пользователь уже сохранил веб-канал, на странице обнаружения не должна отображаться кнопка Сохранить.</span><span class="sxs-lookup"><span data-stu-id="a3af1-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="a3af1-118">Страница обнаружения, представляющая радиоканал, должна проверять свойство **темплатебеингдисплайединлокаллибрари** по той же причине.</span><span class="sxs-lookup"><span data-stu-id="a3af1-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3af1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a3af1-119">Requirements</span></span>



| <span data-ttu-id="a3af1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a3af1-120">Requirement</span></span> | <span data-ttu-id="a3af1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a3af1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3af1-122">Версия</span><span class="sxs-lookup"><span data-stu-id="a3af1-122">Version</span></span><br/> | <span data-ttu-id="a3af1-123">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="a3af1-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="a3af1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a3af1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3af1-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3af1-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3af1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3af1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3af1-127">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="a3af1-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





