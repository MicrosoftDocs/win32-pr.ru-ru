---
title: External. Чанжевиев, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Чанжевиев изменяет представление в проигрывателе Windows Media.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Чанжевиев метод Windows Media Player
- Чанжевиев метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Чанжевиев
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694507"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="c2116-108">External. Чанжевиев, метод</span><span class="sxs-lookup"><span data-stu-id="c2116-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="c2116-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="c2116-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c2116-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2116-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c2116-111">Метод **чанжевиев** изменяет представление в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c2116-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2116-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2116-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="c2116-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2116-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2116-114">*Либрарилокатионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2116-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2116-115">[Константа расположения библиотеки](library-location-constants.md) , указывающая тип нового представления.</span><span class="sxs-lookup"><span data-stu-id="c2116-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="c2116-116">Например, константа Кпженреид указывает, что новое представление будет показывать конкретный жанр.</span><span class="sxs-lookup"><span data-stu-id="c2116-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="c2116-117">*Либрарилокатионид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2116-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2116-118">**Строка** , содержащая идентификатор конкретного элемента, который должен быть отображен в новом представлении.</span><span class="sxs-lookup"><span data-stu-id="c2116-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="c2116-119">Например, если *либрарилокатионтипе* имеет значение кпженреид, этот параметр указывает идентификатор жанра, который будет отображаться в новом представлении.</span><span class="sxs-lookup"><span data-stu-id="c2116-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="c2116-120">Эта строка может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="c2116-120">This string can be empty.</span></span> <span data-ttu-id="c2116-121">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c2116-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c2116-122">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2116-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2116-123">**Строка** , содержащая фильтр для нового представления.</span><span class="sxs-lookup"><span data-stu-id="c2116-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="c2116-124">Представление будет отфильтровано так, как будто пользователь вводит этот текст в элемент управления "колесо слов" игрока.</span><span class="sxs-lookup"><span data-stu-id="c2116-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="c2116-125">Эта строка может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="c2116-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="c2116-126">*Виевпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2116-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2116-127">**Строка** , содержащая параметры, которые проигрыватель Windows Media делает доступным для новой страницы обнаружения, отображаемой с новым представлением.</span><span class="sxs-lookup"><span data-stu-id="c2116-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="c2116-128">Проигрыватель Windows Media не интерпретирует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="c2116-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="c2116-129">Они создаются Интернет-магазином и имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="c2116-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2116-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2116-130">Return value</span></span>

<span data-ttu-id="c2116-131">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c2116-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2116-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2116-132">Remarks</span></span>

<span data-ttu-id="c2116-133">В некоторых случаях имеет смысл присвоить параметру *либрарилокатионид* пустую строку.</span><span class="sxs-lookup"><span data-stu-id="c2116-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="c2116-134">Например, если для параметра *либрарилокатионтипе* задать значение аллкпалбумидс, то новое представление будет представлять все альбомы.</span><span class="sxs-lookup"><span data-stu-id="c2116-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="c2116-135">Отдельный альбом не будет отображаться в новом представлении, поэтому нет необходимости указывать идентификатор альбома в параметре *либрарилокатионид* .</span><span class="sxs-lookup"><span data-stu-id="c2116-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="c2116-136">Параметр *виевпарамс* предоставляет способ связи страницы обнаружения с другой страницей обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c2116-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="c2116-137">Когда сценарий на странице обнаружения вызывает **чанжевиев**, проигрыватель Windows Media корректирует свой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c2116-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="c2116-138">Эта корректировка приводит к тому, что проигрыватель вызывает метод [ивмпконтентпартнер::-Template](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) подключаемого модуля, чтобы получить URL-адрес новой страницы обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c2116-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="c2116-139">Строка, которую передается исходной страницей обнаружения в параметре *виевпарамс* , не передается в метод **DataTemplate**.</span><span class="sxs-lookup"><span data-stu-id="c2116-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="c2116-140">Однако новая страница обнаружения может получить строку *виевпарамс* , вызвав [External. виевпараметерс](external-viewparameters.md).</span><span class="sxs-lookup"><span data-stu-id="c2116-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2116-141">Требования</span><span class="sxs-lookup"><span data-stu-id="c2116-141">Requirements</span></span>



| <span data-ttu-id="c2116-142">Требование</span><span class="sxs-lookup"><span data-stu-id="c2116-142">Requirement</span></span> | <span data-ttu-id="c2116-143">Значение</span><span class="sxs-lookup"><span data-stu-id="c2116-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2116-144">Версия</span><span class="sxs-lookup"><span data-stu-id="c2116-144">Version</span></span><br/> | <span data-ttu-id="c2116-145">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c2116-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c2116-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c2116-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="c2116-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2116-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2116-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2116-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2116-149">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="c2116-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c2116-150">**External. Чанжевиевонлинелист**</span><span class="sxs-lookup"><span data-stu-id="c2116-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="c2116-151">**External. Либрарилокатионид**</span><span class="sxs-lookup"><span data-stu-id="c2116-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="c2116-152">**External. Либрарилокатионтипе**</span><span class="sxs-lookup"><span data-stu-id="c2116-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="c2116-153">**External. Виевпараметерс**</span><span class="sxs-lookup"><span data-stu-id="c2116-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





