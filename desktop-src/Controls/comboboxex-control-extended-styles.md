---
title: Расширенные стили элемента управления ComboBoxEx (Коммктрл. h)
description: Поддержка расширенных стилей, перечисленных в этом разделе, а также большинства стандартных стилей элемента управления "поле со списком".
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651866"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="66bf2-103">Расширенные стили элемента управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="66bf2-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="66bf2-104">Поддержка расширенных стилей, перечисленных в этом разделе, а также большинства стандартных стилей элемента управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="66bf2-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="66bf2-105">Константа</span><span class="sxs-lookup"><span data-stu-id="66bf2-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="66bf2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="66bf2-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="66bf2-107"><dt>**КБЕС \_ ex \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="66bf2-108">Операции поиска **BSTR** в списке будут учитываться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="66bf2-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="66bf2-109">Это включает поиск в результате ввода текста в поле ввода и \_ сообщения ФИНДСТРИНЖЕКСАКТ CB.</span><span class="sxs-lookup"><span data-stu-id="66bf2-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="66bf2-110"><dt>**КБЕС \_ ex \_ ноедитимаже**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="66bf2-111">Поле ввода и раскрывающийся список не будут отображать изображения элементов.</span><span class="sxs-lookup"><span data-stu-id="66bf2-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="66bf2-112"><dt>**КБЕС \_ ex \_ ноедитимажеиндент**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="66bf2-113">Поле ввода и раскрывающийся список не будут отображать изображения элементов.</span><span class="sxs-lookup"><span data-stu-id="66bf2-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="66bf2-114"><dt>**КБЕС \_ ex \_ носизелимит**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="66bf2-115">Позволяет размер элемента управления ComboBoxEx меньше вертикального размера, чем содержащийся в нем элемент управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="66bf2-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="66bf2-116">Если размер ComboBoxEx меньше, чем поле со списком, поле со списком будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="66bf2-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="66bf2-117"><dt>**КБЕС \_ ex \_ пасвордбреакпрок**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="66bf2-118">Только Windows NT.</span><span class="sxs-lookup"><span data-stu-id="66bf2-118">Windows NT only.</span></span> <span data-ttu-id="66bf2-119">В поле ввода будут использоваться символы косой черты (/), обратной косой черты ( \) и точки (.) в качестве разделителей слов.</span><span class="sxs-lookup"><span data-stu-id="66bf2-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="66bf2-120">Это делает возможными сочетания клавиш для перемещения курсора по словам, действующие в именах путей и URL-адресах.</span><span class="sxs-lookup"><span data-stu-id="66bf2-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="66bf2-121"><dt>**КБЕС \_ ex \_ текстенделлипсис**</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="66bf2-122">**Windows Vista и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="66bf2-122">**Windows Vista and later.**</span></span> <span data-ttu-id="66bf2-123">Приводит к тому, что элементы в раскрывающемся списке и поле ввода (если поле ввода доступно только для чтения) усекаются с многоточием ("..."), а не просто обрезаются по границе элемента управления.</span><span class="sxs-lookup"><span data-stu-id="66bf2-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="66bf2-124">Это полезно, когда элементу управления необходимо присвоить фиксированную ширину, но записи в списке могут быть длинными.</span><span class="sxs-lookup"><span data-stu-id="66bf2-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66bf2-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66bf2-125">Remarks</span></span>

<span data-ttu-id="66bf2-126">Расширенные стили ComboBox задаются и извлекаются с помощью [**кбем \_ Сетекстендедстиле**](cbem-setextendedstyle.md) и [**кбем \_ жетекстендедстиле**](cbem-getextendedstyle.md) messages.</span><span class="sxs-lookup"><span data-stu-id="66bf2-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="66bf2-127">Если вы попытаетесь задать расширенный стиль для элемента управления ComboBoxEx, созданного с помощью [**\_ простого стиля CBS**](combo-box-styles.md) , он может не перерисовываться должным образом.</span><span class="sxs-lookup"><span data-stu-id="66bf2-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="66bf2-128">**\_ Простой стиль CBS** также не работает должным образом с \_ \_ расширенным стилем кбес ex пасвордбреакпрок.</span><span class="sxs-lookup"><span data-stu-id="66bf2-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66bf2-129">Требования</span><span class="sxs-lookup"><span data-stu-id="66bf2-129">Requirements</span></span>



| <span data-ttu-id="66bf2-130">Требование</span><span class="sxs-lookup"><span data-stu-id="66bf2-130">Requirement</span></span> | <span data-ttu-id="66bf2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="66bf2-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66bf2-132">Header</span><span class="sxs-lookup"><span data-stu-id="66bf2-132">Header</span></span><br/> | <dl> <span data-ttu-id="66bf2-133"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="66bf2-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





