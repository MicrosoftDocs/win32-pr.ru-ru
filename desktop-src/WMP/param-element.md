---
title: Элемент PARAM (пакет SDK для WMP)
description: Элемент PARAM определяет пользовательский параметр, связанный с списком воспроизведения или элементом списка воспроизведения.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Проигрыватель Windows Media, элемент PARAM
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699095"
---
# <a name="param-element"></a><span data-ttu-id="efb07-104">PARAM, элемент</span><span class="sxs-lookup"><span data-stu-id="efb07-104">PARAM Element</span></span>

<span data-ttu-id="efb07-105">Элемент **param** определяет пользовательский параметр, связанный с списком воспроизведения или элементом списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="efb07-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="efb07-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efb07-106">Parameters</span></span>

<span data-ttu-id="efb07-107">Параметр также можно связать с показом, а не с отдельным клипом, поместив этот элемент непосредственно после тега **ASX** .</span><span class="sxs-lookup"><span data-stu-id="efb07-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="efb07-108">На эти элементы ссылаются имена и значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="efb07-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="efb07-109">Этот элемент **ASX** доступен только для проигрывателя Windows Media версии 6,01 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="efb07-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="efb07-110">Стандартная установка Microsoft Internet Explorer 5 включает совместимую версию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="efb07-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="efb07-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="efb07-111">Attributes</span></span>

<span data-ttu-id="efb07-112">**ИМЯ**</span><span class="sxs-lookup"><span data-stu-id="efb07-112">**NAME**</span></span>

<span data-ttu-id="efb07-113">Имя, используемое для доступа к значению параметра.</span><span class="sxs-lookup"><span data-stu-id="efb07-113">Name used to access the parameter value.</span></span> <span data-ttu-id="efb07-114">Имя может быть любой допустимой строкой.</span><span class="sxs-lookup"><span data-stu-id="efb07-114">The name can be any valid string.</span></span> <span data-ttu-id="efb07-115">Следующие строки уже определены.</span><span class="sxs-lookup"><span data-stu-id="efb07-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="efb07-116">Строка</span><span class="sxs-lookup"><span data-stu-id="efb07-116">String</span></span>                          | <span data-ttu-id="efb07-117">Описание</span><span class="sxs-lookup"><span data-stu-id="efb07-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb07-118">алловшуффле</span><span class="sxs-lookup"><span data-stu-id="efb07-118">AllowShuffle</span></span>                    | <span data-ttu-id="efb07-119">Атрибут **value** указывает, позволяет ли список воспроизведения метафайла проигрывателю Windows Media воспроизвести записи в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="efb07-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="efb07-120">Для атрибута value можно задать **значение** "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="efb07-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="efb07-121">Значение по умолчанию — No.</span><span class="sxs-lookup"><span data-stu-id="efb07-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="efb07-122">канпаусе</span><span class="sxs-lookup"><span data-stu-id="efb07-122">CanPause</span></span>                        | <span data-ttu-id="efb07-123">Атрибут **value** указывает, может ли пользователь приостановить воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="efb07-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="efb07-124">Для атрибута value можно задать **значение** "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="efb07-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="efb07-125">Значение по умолчанию — Yes.</span><span class="sxs-lookup"><span data-stu-id="efb07-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="efb07-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="efb07-126">CanSeek</span></span>                         | <span data-ttu-id="efb07-127">Атрибут **value** указывает, может ли пользователь изменять текущую положение воспроизведения с помощью строки поиска, перемотки вперед или быстро наоборот.</span><span class="sxs-lookup"><span data-stu-id="efb07-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="efb07-128">Для атрибута value можно задать **значение** "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="efb07-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="efb07-129">Значение по умолчанию — Yes.</span><span class="sxs-lookup"><span data-stu-id="efb07-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="efb07-130">канскипбакк</span><span class="sxs-lookup"><span data-stu-id="efb07-130">CanSkipBack</span></span>                     | <span data-ttu-id="efb07-131">Атрибут **value** указывает, может ли пользователь перейти назад к предыдущему элементу списка воспроизведения, нажав кнопку **назад**.</span><span class="sxs-lookup"><span data-stu-id="efb07-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="efb07-132">Для атрибута value можно задать **значение** "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="efb07-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="efb07-133">Значение по умолчанию — Yes.</span><span class="sxs-lookup"><span data-stu-id="efb07-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="efb07-134">канскипфорвард</span><span class="sxs-lookup"><span data-stu-id="efb07-134">CanSkipForward</span></span>                  | <span data-ttu-id="efb07-135">Атрибут **value** указывает, может ли пользователь перейти вперед к следующему элементу списка воспроизведения, нажав кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="efb07-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="efb07-136">Для атрибута value можно задать **значение** "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="efb07-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="efb07-137">Значение по умолчанию — Yes.</span><span class="sxs-lookup"><span data-stu-id="efb07-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="efb07-138">кпрадиоид</span><span class="sxs-lookup"><span data-stu-id="efb07-138">CPRadioID</span></span>                       | <span data-ttu-id="efb07-139">Атрибут **value** указывает идентификатор радиоканала, предоставленного интернет-магазином типа 1.</span><span class="sxs-lookup"><span data-stu-id="efb07-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="efb07-140">То есть атрибут **value** должен быть равен полю радиоид одного из каналов в каталоге интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="efb07-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="efb07-141">Родительский элемент — это элемент **ASX** .</span><span class="sxs-lookup"><span data-stu-id="efb07-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="efb07-142">Кодирование</span><span class="sxs-lookup"><span data-stu-id="efb07-142">Encoding</span></span>                        | <span data-ttu-id="efb07-143">Атрибут **value имеет значение** "UTF-8", чтобы указать, что метафайл является файлом в кодировке Юникод (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="efb07-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="efb07-144">хтмлфлинк</span><span class="sxs-lookup"><span data-stu-id="efb07-144">HtmlFlink</span></span>                       | <span data-ttu-id="efb07-145">Атрибут **value** представляет собой строку, предоставленную Интернет-магазином типа 1.</span><span class="sxs-lookup"><span data-stu-id="efb07-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="efb07-146">Проигрыватель Windows Media передает строку методу [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , который реализуется подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="efb07-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="efb07-147">Метод **GetItemInfo** возвращает URL-адрес веб-страницы, отображаемой на панели **воспроизведения** проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="efb07-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="efb07-148">Веб-страница имеет доступ ко всем методам, которые **внешний** объект предоставляет для хранилищ типа 1.</span><span class="sxs-lookup"><span data-stu-id="efb07-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="efb07-149">Список этих методов см. в разделе [внешний объект для Интернет-магазинов типа 1](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="efb07-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="efb07-150">хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="efb07-150">HTMLView</span></span>                        | <span data-ttu-id="efb07-151">Атрибут **value** задает URL-адрес, отображаемый на панели воспроизведение в проигрывателе полноэкранного режима на время **показа** списка воспроизведения или текущей записи в зависимости от того, является ли родительский элемент элементом **ASX** или элементом **entry** .</span><span class="sxs-lookup"><span data-stu-id="efb07-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="efb07-152">Хтмлвиев не поддерживается для элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="efb07-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="efb07-153">Журнал:*fieldname* \[ :*пространство имен*\]</span><span class="sxs-lookup"><span data-stu-id="efb07-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="efb07-154">Атрибут **value** указывает значение, которое будет задано для указанного поля журнала.</span><span class="sxs-lookup"><span data-stu-id="efb07-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="efb07-155">Область:*пространство имен* атрибута **Name** является необязательной.</span><span class="sxs-lookup"><span data-stu-id="efb07-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="efb07-156">Предбуферная</span><span class="sxs-lookup"><span data-stu-id="efb07-156">Prebuffer</span></span>                       | <span data-ttu-id="efb07-157">Атрибут **value** указывает, начинает ли следующий элемент списка воспроизведения буферизацию до конца текущей записи, что обеспечивает простой переход.</span><span class="sxs-lookup"><span data-stu-id="efb07-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="efb07-158">Для атрибута value можно задать **значение** "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="efb07-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="efb07-159">шоввхилебуфферинг</span><span class="sxs-lookup"><span data-stu-id="efb07-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="efb07-160">Атрибут **value** указывает, будет ли отображаться файл изображения, на который ссылается текущий элемент **entry** , до момента, когда следующая запись списка воспроизведения помещается в буфер.</span><span class="sxs-lookup"><span data-stu-id="efb07-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="efb07-161">Для атрибута value можно задать **значение** "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="efb07-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="efb07-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="efb07-162">**VALUE**</span></span>

<span data-ttu-id="efb07-163">Значение, связанное с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="efb07-163">Value associated with this parameter.</span></span> <span data-ttu-id="efb07-164">Это может быть либо числовое, либо строковое значение.</span><span class="sxs-lookup"><span data-stu-id="efb07-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="efb07-165">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="efb07-165">Parent/Child Elements</span></span>



| <span data-ttu-id="efb07-166">Иерархия</span><span class="sxs-lookup"><span data-stu-id="efb07-166">Hierarchy</span></span>       | <span data-ttu-id="efb07-167">Элементы</span><span class="sxs-lookup"><span data-stu-id="efb07-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="efb07-168">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="efb07-168">Parent elements</span></span> | <span data-ttu-id="efb07-169">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="efb07-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="efb07-170">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="efb07-170">Child elements</span></span>  | <span data-ttu-id="efb07-171">Нет</span><span class="sxs-lookup"><span data-stu-id="efb07-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="efb07-172">Remarks</span><span class="sxs-lookup"><span data-stu-id="efb07-172">Remarks</span></span>

<span data-ttu-id="efb07-173">Этот элемент позволяет пользователям размещать дополнительные сведения о каждом клипе в элементе **entry** , содержащем его.</span><span class="sxs-lookup"><span data-stu-id="efb07-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="efb07-174">Для получения сведений о метаданных, указанных в **записи** списка воспроизведения, используйте *носитель*. метод **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="efb07-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="efb07-175">*Носитель*. метод **getItemInfo** извлекает значение атрибута **value** по заданному имени параметра.</span><span class="sxs-lookup"><span data-stu-id="efb07-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="efb07-176">Предыдущие версии проигрывателя Windows Media извлекают сведения о метаданных, указанные в **записи** списка воспроизведения, используя метод **жетмедиапараметер** , задавая имя параметра и номер индекса для записи.</span><span class="sxs-lookup"><span data-stu-id="efb07-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="efb07-177">Параметр также можно связать с показом, а не с отдельным клипом, поместив этот элемент непосредственно после тега **ASX** .</span><span class="sxs-lookup"><span data-stu-id="efb07-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="efb07-178">На эти элементы ссылаются имена и значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="efb07-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="efb07-179">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="efb07-179">**Note**</span></span>

<span data-ttu-id="efb07-180">Этот элемент **ASX** доступен только для проигрывателя Windows Media версии 6,01 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="efb07-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="efb07-181">Стандартная установка Microsoft Internet Explorer 5 включает совместимую версию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="efb07-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="efb07-182">Примеры</span><span class="sxs-lookup"><span data-stu-id="efb07-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="efb07-183">Требования</span><span class="sxs-lookup"><span data-stu-id="efb07-183">Requirements</span></span>



| <span data-ttu-id="efb07-184">Требование</span><span class="sxs-lookup"><span data-stu-id="efb07-184">Requirement</span></span> | <span data-ttu-id="efb07-185">Значение</span><span class="sxs-lookup"><span data-stu-id="efb07-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb07-186">Версия</span><span class="sxs-lookup"><span data-stu-id="efb07-186">Version</span></span><br/> | <span data-ttu-id="efb07-187">Проигрыватель Windows Media версии 7,0 или более поздней, для предварительно определенных имен (Канпаусе, CanSeek, Канскипбакк и Канскипфорвард) требуется проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="efb07-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efb07-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efb07-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb07-189">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="efb07-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="efb07-190">**Ведение журнала данных потока**</span><span class="sxs-lookup"><span data-stu-id="efb07-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="efb07-191">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="efb07-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="efb07-192">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="efb07-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





