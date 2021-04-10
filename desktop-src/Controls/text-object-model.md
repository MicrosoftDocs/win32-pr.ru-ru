---
title: Объектная модель текста
description: В этом разделе содержатся сведения об элементах программирования, используемых с моделью текстовых объектов (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103891184"
---
# <a name="text-object-model"></a><span data-ttu-id="adf10-103">Объектная модель текста</span><span class="sxs-lookup"><span data-stu-id="adf10-103">Text Object Model</span></span>

<span data-ttu-id="adf10-104">В этом разделе содержатся сведения об элементах программирования, используемых с моделью текстовых объектов (TOM).</span><span class="sxs-lookup"><span data-stu-id="adf10-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="adf10-105">TOM определяет значительный набор интерфейсов обработки текста.</span><span class="sxs-lookup"><span data-stu-id="adf10-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="adf10-106">Текстовые решения, такие как Microsoft Word и элементы управления Rich Edit, поддерживают набор компонентов TOM.</span><span class="sxs-lookup"><span data-stu-id="adf10-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="adf10-107">На том было сильно влияло на WordBasic (язык программирования, используемый для Word), и его легко использовать в Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="adf10-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="adf10-108">Эта совместимость имеет несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="adf10-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="adf10-109">Код может легко переноситься из одного решения в другое.</span><span class="sxs-lookup"><span data-stu-id="adf10-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="adf10-110">Один язык можно использовать для обмена текстовыми данными между различными текстовыми обработчиками.</span><span class="sxs-lookup"><span data-stu-id="adf10-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="adf10-111">Это снижает потребность в документации и коде по сравнению с отдельными интерфейсами модели COM и VBA.</span><span class="sxs-lookup"><span data-stu-id="adf10-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="adf10-112">Однако это может быть менее эффективным для целей C/C++, чем использование более общих COM-интерфейсов нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="adf10-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="adf10-113">TOM — это простой набор интерфейсов для реализации в основных текстовых решениях, Word и форматированных элементах редактирования.</span><span class="sxs-lookup"><span data-stu-id="adf10-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="adf10-114">Однако для приложений, которые размещают небольшое внимание на текст, лучше предоставить объект TOM, передавая текст в элемент управления Edit, который поддерживает TOM.</span><span class="sxs-lookup"><span data-stu-id="adf10-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="adf10-115">Так как широкие возможности управления редактированием поставляются с операционными системами Майкрософт, они являются стандартными средствами для получения функции TOM.</span><span class="sxs-lookup"><span data-stu-id="adf10-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="adf10-116">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="adf10-116">Overviews</span></span>



| <span data-ttu-id="adf10-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="adf10-117">Topic</span></span>                                                          | <span data-ttu-id="adf10-118">Содержимое</span><span class="sxs-lookup"><span data-stu-id="adf10-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adf10-119">О модели текстовых объектов</span><span class="sxs-lookup"><span data-stu-id="adf10-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="adf10-120">Объект модели текстовых объектов верхнего уровня (TOM) определяется интерфейсом [**итекстдокумент**](/windows/desktop/api/Tom/nn-tom-itextdocument) , который имеет методы для создания и извлечения объектов в иерархии объектов ниже.</span><span class="sxs-lookup"><span data-stu-id="adf10-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="adf10-121">Использование объектной модели текста</span><span class="sxs-lookup"><span data-stu-id="adf10-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="adf10-122">Примеры кода в этом документе показывают различные аспекты использования объектной модели текста (TOM).</span><span class="sxs-lookup"><span data-stu-id="adf10-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="adf10-123">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="adf10-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf10-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="adf10-124">Topic</span></span></th>
<th><span data-ttu-id="adf10-125">Содержимое</span><span class="sxs-lookup"><span data-stu-id="adf10-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adf10-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="adf10-127">Интерфейс <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> — это интерфейс верхнего уровня Tom, который получает активные объекты выделения и диапазона для любой истории в документе независимо от того, активна или нет.</span><span class="sxs-lookup"><span data-stu-id="adf10-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="adf10-128">Он позволяет приложению выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="adf10-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="adf10-129">Открытие и сохранение документов.</span><span class="sxs-lookup"><span data-stu-id="adf10-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="adf10-130">Управление поведением отмены и обновлением экрана.</span><span class="sxs-lookup"><span data-stu-id="adf10-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="adf10-131">Поиск диапазона по положению экрана.</span><span class="sxs-lookup"><span data-stu-id="adf10-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="adf10-132">Получение перечислителя истории <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="adf10-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="adf10-133"><strong>Когда следует реализовывать</strong></span><span class="sxs-lookup"><span data-stu-id="adf10-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="adf10-134">Обычно приложения не реализуют интерфейс <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="adf10-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="adf10-135">Microsoft Text Solutions, например элементы управления Rich Editing, реализуют <strong>итекстдокумент</strong> как часть своей реализации Tom.</span><span class="sxs-lookup"><span data-stu-id="adf10-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="adf10-136"><strong>Когда следует использовать</strong></span><span class="sxs-lookup"><span data-stu-id="adf10-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="adf10-137">Приложения могут извлекать указатель <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> из элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="adf10-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="adf10-138">Для этого отправьте <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> сообщение, чтобы получить объект <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>иричедитоле</strong></a> из элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="adf10-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="adf10-139">Затем вызовите метод <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> объекта, чтобы получить указатель <strong>итекстдокумент</strong> .</span><span class="sxs-lookup"><span data-stu-id="adf10-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf10-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="adf10-141">Доступ к атрибутам диапазона форматированного текста осуществляется через пару сдвоенных интерфейсов, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a> и <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="adf10-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf10-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="adf10-143">Доступ к атрибутам диапазона форматированного текста осуществляется через пару сдвоенных интерфейсов, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a> и <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="adf10-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf10-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>итекстранже</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="adf10-145">Объекты <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>итекстранже</strong></a> — это мощные средства редактирования и привязки данных, позволяющие программе выбирать текст в истории, а затем проверять или изменять этот текст.</span><span class="sxs-lookup"><span data-stu-id="adf10-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf10-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>итекстселектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="adf10-147">Выделение текста — это текстовый диапазон с выделением выделения.</span><span class="sxs-lookup"><span data-stu-id="adf10-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf10-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a></span><span class="sxs-lookup"><span data-stu-id="adf10-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="adf10-149">Целью интерфейса <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a> является перечисление историй в <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="adf10-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

