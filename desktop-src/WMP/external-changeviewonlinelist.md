---
title: External. Чанжевиевонлинелист, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Чанжевиевонлинелист, метод
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- Чанжевиевонлинелист метод Windows Media Player
- Чанжевиевонлинелист метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Чанжевиевонлинелист
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698888"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="64e7e-107">External. Чанжевиевонлинелист, метод</span><span class="sxs-lookup"><span data-stu-id="64e7e-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="64e7e-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="64e7e-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="64e7e-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="64e7e-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="64e7e-110">Метод **чанжевиевонлинелист** изменяет представление в проигрывателе Windows Media для отображения списка, созданного динамически в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="64e7e-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e7e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64e7e-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="64e7e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="64e7e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e7e-113">*Либрарилокатионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-114">[Константа расположения библиотеки](library-location-constants.md) , указывающая тип нового представления.</span><span class="sxs-lookup"><span data-stu-id="64e7e-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="64e7e-115">Например, константа Кпженреид указывает, что новое представление будет показывать конкретный жанр.</span><span class="sxs-lookup"><span data-stu-id="64e7e-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="64e7e-116">*Либрарилокатионид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-117">**Строка** , содержащая идентификатор конкретного элемента, который должен быть отображен в новом представлении.</span><span class="sxs-lookup"><span data-stu-id="64e7e-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="64e7e-118">Например, если *либрарилокатионтипе* имеет значение кпженреид, этот параметр указывает идентификатор жанра, который будет отображаться в новом представлении.</span><span class="sxs-lookup"><span data-stu-id="64e7e-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="64e7e-119">Эта строка может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="64e7e-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="64e7e-120">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-121">**Строка** , содержащая параметры, которые проигрыватель Windows Media передает в подключаемый модуль интернет-магазина путем вызова [ивмпконтентпартнер::-Template](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span><span class="sxs-lookup"><span data-stu-id="64e7e-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="64e7e-122">Проигрыватель Windows Media не интерпретирует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="64e7e-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="64e7e-123">Они создаются Интернет-магазином и имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="64e7e-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="64e7e-124">Эта строка может быть пустой</span><span class="sxs-lookup"><span data-stu-id="64e7e-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="64e7e-125">*FriendlyName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-126">**Строка** , содержащая понятное имя, которое будет отображаться проигрывателем Windows Media для динамического списка.</span><span class="sxs-lookup"><span data-stu-id="64e7e-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="64e7e-127">*Листтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-128">Константа расположения библиотеки, указывающая тип элементов в динамически создаваемом списке.</span><span class="sxs-lookup"><span data-stu-id="64e7e-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="64e7e-129">Например, если значение этого параметра — Кптраккид, то динамический список будет содержать записи.</span><span class="sxs-lookup"><span data-stu-id="64e7e-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="64e7e-130">*ViewMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e7e-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e7e-131">**Строка** , указывающая режим, который проигрыватель Windows Media будет использовать для вывода динамического списка.</span><span class="sxs-lookup"><span data-stu-id="64e7e-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="64e7e-132">Вызывающий объект должен присвоить этому параметру одно из следующих значений, определенных в контентпартнер. h:</span><span class="sxs-lookup"><span data-stu-id="64e7e-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="64e7e-133">виевмодерепорт</span><span class="sxs-lookup"><span data-stu-id="64e7e-133">ViewModeReport</span></span>

<span data-ttu-id="64e7e-134">виевмодедетаилс</span><span class="sxs-lookup"><span data-stu-id="64e7e-134">ViewModeDetails</span></span>

<span data-ttu-id="64e7e-135">виевмодеикон</span><span class="sxs-lookup"><span data-stu-id="64e7e-135">ViewModeIcon</span></span>

<span data-ttu-id="64e7e-136">виевмодетиле</span><span class="sxs-lookup"><span data-stu-id="64e7e-136">ViewModeTile</span></span>

<span data-ttu-id="64e7e-137">виевмодеордередлист</span><span class="sxs-lookup"><span data-stu-id="64e7e-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e7e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64e7e-138">Return value</span></span>

<span data-ttu-id="64e7e-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="64e7e-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e7e-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64e7e-140">Remarks</span></span>

<span data-ttu-id="64e7e-141">Когда сценарий на странице обнаружения вызывает **чанжевиевонлинелист**, проигрыватель Windows Media передает некоторые параметры в методы [Ивмпконтентпартнер:: жетлистконтентс](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) и [ивмпконтентпартнер::-Template](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , которые реализуются подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="64e7e-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="64e7e-142">В следующей таблице показано соответствие между параметрами трех методов.</span><span class="sxs-lookup"><span data-stu-id="64e7e-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="64e7e-143">Чанжевиевонлинелист, параметр</span><span class="sxs-lookup"><span data-stu-id="64e7e-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="64e7e-144">Жетлистконтентс, параметр</span><span class="sxs-lookup"><span data-stu-id="64e7e-144">GetListContents parameter</span></span> | <span data-ttu-id="64e7e-145">Параметр DataTemplate</span><span class="sxs-lookup"><span data-stu-id="64e7e-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="64e7e-146">*локатионтипе*</span><span class="sxs-lookup"><span data-stu-id="64e7e-146">*LocationType*</span></span>                 | <span data-ttu-id="64e7e-147">*расположение*</span><span class="sxs-lookup"><span data-stu-id="64e7e-147">*location*</span></span>                | <span data-ttu-id="64e7e-148">*расположение*</span><span class="sxs-lookup"><span data-stu-id="64e7e-148">*location*</span></span>            |
| <span data-ttu-id="64e7e-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="64e7e-149">*LocationID*</span></span>                   | <span data-ttu-id="64e7e-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="64e7e-150">*pContext*</span></span>                | <span data-ttu-id="64e7e-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="64e7e-151">*pContext*</span></span>            |
| <span data-ttu-id="64e7e-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="64e7e-152">*Params*</span></span>                       | <span data-ttu-id="64e7e-153">*бстрпарамс*</span><span class="sxs-lookup"><span data-stu-id="64e7e-153">*bstrParams*</span></span>              | <span data-ttu-id="64e7e-154">*бстрвиевпарамс*</span><span class="sxs-lookup"><span data-stu-id="64e7e-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="64e7e-155">*листтипе*</span><span class="sxs-lookup"><span data-stu-id="64e7e-155">*ListType*</span></span>                     | <span data-ttu-id="64e7e-156">*бстрлисттипе*</span><span class="sxs-lookup"><span data-stu-id="64e7e-156">*bstrListType*</span></span>            | <span data-ttu-id="64e7e-157">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="64e7e-157">not applicable</span></span>        |



 

<span data-ttu-id="64e7e-158">Поскольку все три метода, показанные в предыдущей таблице, реализуются Интернет-магазином, у вас есть гибкость в использовании параметров.</span><span class="sxs-lookup"><span data-stu-id="64e7e-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="64e7e-159">Идея состоит в том, что вы предоставляете достаточно информации для **жетлистконтентс** , чтобы определить, какой список следует получить, а для- **template** — чтобы определить, какая страница обнаружения должна отображаться далее.</span><span class="sxs-lookup"><span data-stu-id="64e7e-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="64e7e-160">В следующих примерах показаны две возможности.</span><span class="sxs-lookup"><span data-stu-id="64e7e-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="64e7e-161">**Пример 1. динамический список, который находится в каталоге интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="64e7e-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="64e7e-162">Предположим, требуется, чтобы подключаемый модуль получил содержимое динамического списка с ИДЕНТИФИКАТОРом 6 в каталоге интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="64e7e-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="64e7e-163">Предположим, что List 6 представляет собой список дорожек.</span><span class="sxs-lookup"><span data-stu-id="64e7e-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="64e7e-164">Вы можете предоставить подключаемый модуль с достаточной информацией, выполнив следующий вызов.</span><span class="sxs-lookup"><span data-stu-id="64e7e-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="64e7e-165">Обратите внимание, что параметр *params* пуст; у подключаемого модуля достаточно информации в других параметрах.</span><span class="sxs-lookup"><span data-stu-id="64e7e-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="64e7e-166">**Пример 2. динамический список, не накоторыйся в каталоге интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="64e7e-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="64e7e-167">Предположим, вы хотите, чтобы подключаемый модуль получил содержимое динамического списка, не начисленного в каталоге интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="64e7e-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="64e7e-168">Возможно, вы решили иметь динамический список, содержащий песни, выбранные определенным исполнителем.</span><span class="sxs-lookup"><span data-stu-id="64e7e-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="64e7e-169">Предположим, что исполнитель имеет идентификатор 2 в каталоге интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="64e7e-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="64e7e-170">Можно выполнить следующий вызов.</span><span class="sxs-lookup"><span data-stu-id="64e7e-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="64e7e-171">Обратите внимание, что параметры *локатионтипе* и *LocationID* не указывают список.</span><span class="sxs-lookup"><span data-stu-id="64e7e-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="64e7e-172">Вместо этого параметр *params* задает список.</span><span class="sxs-lookup"><span data-stu-id="64e7e-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="64e7e-173">Параметры *локатионтипе* и *LocationID* передаются в **ивмпконтентпартнер:: жетлистконтентс**, но в этом случае **жетлистконтентс** могут игнорировать их.</span><span class="sxs-lookup"><span data-stu-id="64e7e-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="64e7e-174">Параметры *локатионтипе* и *LocationID* также передаются в **ивмпконтентпартнер::-Template**, с помощью которых можно определить, какая страница обнаружения должна отображаться с динамическим списком.</span><span class="sxs-lookup"><span data-stu-id="64e7e-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e7e-175">Требования</span><span class="sxs-lookup"><span data-stu-id="64e7e-175">Requirements</span></span>



| <span data-ttu-id="64e7e-176">Требование</span><span class="sxs-lookup"><span data-stu-id="64e7e-176">Requirement</span></span> | <span data-ttu-id="64e7e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="64e7e-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64e7e-178">Версия</span><span class="sxs-lookup"><span data-stu-id="64e7e-178">Version</span></span><br/> | <span data-ttu-id="64e7e-179">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="64e7e-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="64e7e-180">DLL</span><span class="sxs-lookup"><span data-stu-id="64e7e-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="64e7e-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e7e-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e7e-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64e7e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e7e-183">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="64e7e-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="64e7e-184">**Ивмпконтентпартнер:: Жетлистконтентс**</span><span class="sxs-lookup"><span data-stu-id="64e7e-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="64e7e-185">**Ивмпконтентпартнеркаллбакк:: Аддлистконтентс**</span><span class="sxs-lookup"><span data-stu-id="64e7e-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="64e7e-186">**Ивмпконтентпартнер:: DataTemplate**</span><span class="sxs-lookup"><span data-stu-id="64e7e-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="64e7e-187">**Расположение и выбранный элемент**</span><span class="sxs-lookup"><span data-stu-id="64e7e-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





