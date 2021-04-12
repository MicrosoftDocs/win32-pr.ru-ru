---
title: Сообщение EM_INSERTTABLE (RichEdit. h)
description: Вставляет одну или несколько идентичных строк таблицы с пустыми ячейками.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Элементы управления Windows для EM_INSERTTABLE сообщений
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489447"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="9c0c1-104">\_Сообщение ИНСЕРТТАБЛЕ EM</span><span class="sxs-lookup"><span data-stu-id="9c0c1-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="9c0c1-105">Вставляет одну или несколько идентичных строк таблицы с пустыми ячейками.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="9c0c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c0c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c0c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c0c1-108">Указатель на структуру [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="9c0c1-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c0c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c0c1-110">Указатель на структуру [**таблецеллпармс**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="9c0c1-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0c1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c0c1-111">Return value</span></span>

<span data-ttu-id="9c0c1-112">Возвращает значение S \_ ОК, если таблица вставлена, или код ошибки, если нет.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0c1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c0c1-113">Remarks</span></span>

<span data-ttu-id="9c0c1-114">Если элемент **кпстартров** объекта [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) равен 1, это сообщение удаляет выбранный текст (если он есть), а затем вставляет пустые строки таблицы с параметрами строки и ячейки, заданными параметром *wParam* и *lParam*.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="9c0c1-115">Он оставляет выбор, указывающий на начало первой ячейки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="9c0c1-116">После этого клиент может заполнить ячейки таблицы, наведя выбор (или [**итекстранже**](/windows/desktop/api/Tom/nn-tom-itextrange)) на различные концы ячейки, а также вставив и отформатировать нужный текст.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="9c0c1-117">Такой текст может включать строки вложенной таблицы.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-117">Such text can include nested table rows.</span></span> <span data-ttu-id="9c0c1-118">Кроме того, если элемент **Кпстартров** **таблеровпармс** имеет значение 0 или больше, строки таблицы вставляются в позиции символа, заданного параметром **кпстартров**.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="9c0c1-119">Это изменяет текущий выбор только в том случае, если таблица вставлена в выделенный текст.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="9c0c1-120">Таблица Microsoft Rich Edit состоит из последовательности строк таблицы, в свою очередь состоящей из последовательностей абзацев.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="9c0c1-121">Строка таблицы начинается с специального абзаца-разделителя из двух символов U + FFF9 U + 000D и заканчивается в абзаце-разделителе с двумя символами U + ФФФБ U + 000D.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="9c0c1-122">Каждая ячейка завершается символом ячейки U + 0007, которая рассматривается как жесткая конечная знак абзаца так же, как U + 000D (CR).</span><span class="sxs-lookup"><span data-stu-id="9c0c1-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="9c0c1-123">Параметры строк и ячеек таблицы рассматриваются как специальные форматирование абзаца для разделителей строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="9c0c1-124">Форматирование содержит сведения в структуре [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="9c0c1-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="9c0c1-125">Параметры ячейки, заданные структурой [**таблецеллпармс**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) , хранятся в расширенной версии массива вкладок.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="9c0c1-126">Этот формат позволяет вкладывать таблицы в другие таблицы с глубиной до пятнадцати уровней.</span><span class="sxs-lookup"><span data-stu-id="9c0c1-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0c1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9c0c1-127">Requirements</span></span>



| <span data-ttu-id="9c0c1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9c0c1-128">Requirement</span></span> | <span data-ttu-id="9c0c1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9c0c1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0c1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c0c1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0c1-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9c0c1-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9c0c1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c0c1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0c1-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9c0c1-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c0c1-134">Header</span><span class="sxs-lookup"><span data-stu-id="9c0c1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c0c1-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c1-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c0c1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c0c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0c1-137">**EM \_ инсертимаже**</span><span class="sxs-lookup"><span data-stu-id="9c0c1-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





