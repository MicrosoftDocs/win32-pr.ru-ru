---
description: После оценки стратегии свойств необходимо определить, какие свойства должны отображаться в пользовательском интерфейсе проводника Windows и где.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Использование списков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991549"
---
# <a name="using-property-lists"></a><span data-ttu-id="19678-103">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="19678-103">Using Property Lists</span></span>

<span data-ttu-id="19678-104">После оценки стратегии свойств необходимо определить, какие свойства должны отображаться в пользовательском интерфейсе проводника Windows и где.</span><span class="sxs-lookup"><span data-stu-id="19678-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="19678-105">Существуют различные расположения, где свойства отображаются в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="19678-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="19678-106">Изменение свойства, с другой стороны, включено только в диалоговом окне **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="19678-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="19678-107">Это диалоговое окно можно вызвать с помощью ссылки **изменить свойства** в **области просмотра** или в контекстном меню элемента.</span><span class="sxs-lookup"><span data-stu-id="19678-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="19678-108">Списки свойств являются строками, разделенными точкой с запятой, которые имеют следующую форму.</span><span class="sxs-lookup"><span data-stu-id="19678-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="19678-109">В следующей таблице показан единственный доступный в данный момент флаг.</span><span class="sxs-lookup"><span data-stu-id="19678-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="19678-110">Flag</span><span class="sxs-lookup"><span data-stu-id="19678-110">Flag</span></span> | <span data-ttu-id="19678-111">Описание</span><span class="sxs-lookup"><span data-stu-id="19678-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="19678-112">Не выводите свойство на **панели предварительного просмотра** , как указано в значении раздела реестра **превиевдетаилс** .</span><span class="sxs-lookup"><span data-stu-id="19678-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="19678-113">Если значение этого свойства не задано, см. пример, следующий за следующей таблицей.</span><span class="sxs-lookup"><span data-stu-id="19678-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="19678-114">После определения списка свойств можно сохранить эту строку в реестре с помощью стандартной системы [сопоставления файлов оболочки](../shell/fa-file-types.md) в **\_ \_ корне классов hKey.**</span><span class="sxs-lookup"><span data-stu-id="19678-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="19678-115">В следующей таблице перечислены значения для списков свойств, которые могут быть назначены в разделе реестра для определенного расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="19678-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19678-116">Значение</span><span class="sxs-lookup"><span data-stu-id="19678-116">Value</span></span></th>
<th><span data-ttu-id="19678-117">Описание</span><span class="sxs-lookup"><span data-stu-id="19678-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19678-118">фуллдетаилс</span><span class="sxs-lookup"><span data-stu-id="19678-118">FullDetails</span></span></td>
<td><span data-ttu-id="19678-119">Свойства отображаются на вкладке <strong>сведения</strong> диалогового окна <strong>свойства</strong> .</span><span class="sxs-lookup"><span data-stu-id="19678-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="19678-120">Это полный список свойств, поддерживаемых типом файлов.</span><span class="sxs-lookup"><span data-stu-id="19678-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19678-121">превиевдетаилс</span><span class="sxs-lookup"><span data-stu-id="19678-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="19678-122">Свойства отображаются в <strong>области просмотра</strong>.</span><span class="sxs-lookup"><span data-stu-id="19678-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19678-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="19678-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="19678-124">Свойства отображаются в области заголовка <strong>области предварительного просмотра</strong> рядом с эскизом элемента.</span><span class="sxs-lookup"><span data-stu-id="19678-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="19678-125">Максимальное число записей равно 3.</span><span class="sxs-lookup"><span data-stu-id="19678-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="19678-126">Если список свойств содержит больше максимально допустимого числа, остальные записи игнорируются.</span><span class="sxs-lookup"><span data-stu-id="19678-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19678-127">тилеинфо</span><span class="sxs-lookup"><span data-stu-id="19678-127">TileInfo</span></span></td>
<td><span data-ttu-id="19678-128">Свойства отображаются, когда представление списка находится в режиме просмотра <strong>плиток</strong> .</span><span class="sxs-lookup"><span data-stu-id="19678-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="19678-129">Максимальное число записей равно 3.</span><span class="sxs-lookup"><span data-stu-id="19678-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="19678-130">Если список свойств содержит больше максимально допустимого числа, остальные записи игнорируются.</span><span class="sxs-lookup"><span data-stu-id="19678-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19678-131">Это значение присутствовало в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19678-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19678-132">екстендедтилеинфо</span><span class="sxs-lookup"><span data-stu-id="19678-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="19678-133">Свойства элемента отображаются, когда представление списка находится в режиме <strong>расширенного представления мозаики</strong> .</span><span class="sxs-lookup"><span data-stu-id="19678-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19678-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="19678-134">InfoTip</span></span></td>
<td><span data-ttu-id="19678-135">Свойства отображаются во всплывающей подсказке, когда пользователь наводит указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="19678-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19678-136">Это значение присутствовало в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19678-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19678-137">куикктип</span><span class="sxs-lookup"><span data-stu-id="19678-137">QuickTip</span></span></td>
<td><span data-ttu-id="19678-138">Свойства отображаются, когда трудно получить свойства непосредственно из элемента, например при доступе к элементу через низкое сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="19678-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="19678-139">Рекомендуется, чтобы свойства с именем, такие как тип или размер, не требовали открытия файлового потока для определения их значения.</span><span class="sxs-lookup"><span data-stu-id="19678-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19678-140">Это значение присутствовало в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19678-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="19678-141">В приведенном ниже примере определяется значение Превиевдетаилс для типа файла рецепта с помощью ProgID **реЦипекэй**.</span><span class="sxs-lookup"><span data-stu-id="19678-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="19678-142">Как описано в разделе о [взаимосвязи файлов оболочки](../shell/fa-file-types.md) , сопоставления файлов можно описать наиболее подчисленной для наиболее общей формы.</span><span class="sxs-lookup"><span data-stu-id="19678-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="19678-143">Наиболее конкретная форма — это расширение имени файла, а наиболее универсальная форма — это ключ, который применяется ко всем файлам и папкам.</span><span class="sxs-lookup"><span data-stu-id="19678-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="19678-144">Между этими двумя экстремальными значениями можно также определить [идентификатор ProgID](../shell/fa-progids.md) , который группирует набор расширений имен файлов (например, типы JPG и JPEG, сгруппированные как **жпегфиле**).</span><span class="sxs-lookup"><span data-stu-id="19678-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="19678-145">При определении списков свойств необходимо определить их для ProgID или, в некоторых случаях, для определенных расширений имен файлов.</span><span class="sxs-lookup"><span data-stu-id="19678-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="19678-146">Старайтесь не полагаться на обширные записи, такие как ключ **аллфилесистемобжектс** .</span><span class="sxs-lookup"><span data-stu-id="19678-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19678-147">См. также</span><span class="sxs-lookup"><span data-stu-id="19678-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19678-148">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="19678-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="19678-149">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="19678-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="19678-150">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="19678-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="19678-151">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="19678-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="19678-152">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="19678-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
