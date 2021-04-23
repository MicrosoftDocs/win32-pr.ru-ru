---
title: Сообщение EM_SETTABLEPARMS (RichEdit. h)
description: Изменяет параметры строк в таблице.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Элементы управления Windows для EM_SETTABLEPARMS сообщений
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988486"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="9a234-104">\_Сообщение СЕТТАБЛЕПАРМС EM</span><span class="sxs-lookup"><span data-stu-id="9a234-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="9a234-105">Изменяет параметры строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a234-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a234-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a234-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a234-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a234-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a234-108">Указатель на структуру [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="9a234-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a234-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a234-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a234-110">Указатель на структуру [**таблецеллпармс**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="9a234-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a234-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a234-111">Return value</span></span>

<span data-ttu-id="9a234-112">\_При успешном выполнении или один из следующих кодов ошибок возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="9a234-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="9a234-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9a234-113">Return code</span></span>                                                                                    | <span data-ttu-id="9a234-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9a234-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a234-115"><dt>**Д \_ Не пройден**</dt></span><span class="sxs-lookup"><span data-stu-id="9a234-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="9a234-116">Невозможно внести изменения.</span><span class="sxs-lookup"><span data-stu-id="9a234-116">Changes cannot be made.</span></span> <span data-ttu-id="9a234-117">Это может произойти, если элемент управления является обычным текстовым или однострочным или если точка вставки находится внутри математического объекта.</span><span class="sxs-lookup"><span data-stu-id="9a234-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="9a234-118">Это также происходит, если таблицы отключены или сообщение [**EM \_ сетедитстиликс**](em-seteditstyleex.md) задает значимое значение **SES \_ ex \_** .</span><span class="sxs-lookup"><span data-stu-id="9a234-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="9a234-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9a234-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="9a234-120">Параметр *wParam* или *lParam* имеет значение null или указывает на недопустимую структуру.</span><span class="sxs-lookup"><span data-stu-id="9a234-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="9a234-121">Элемент **кцелл** структуры [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) должен содержать не менее 1 и не более 63.</span><span class="sxs-lookup"><span data-stu-id="9a234-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="9a234-122">Элемент **кбров** должен равняться `sizeof(TABLEROWPARMS)` или `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="9a234-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="9a234-123">Последнее значение — это размер структуры RichEdit 4,1 **таблеровпармс** .</span><span class="sxs-lookup"><span data-stu-id="9a234-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="9a234-124">Элемент **кбцелл** объекта **таблеровпармс** должен равняться `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="9a234-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="9a234-125">Точка вставки должна находиться в начале таблицы или в строке таблицы, а количество ячеек может быть изменено только на единицу.</span><span class="sxs-lookup"><span data-stu-id="9a234-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="9a234-126"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a234-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="9a234-127">Недостаточно свободной памяти.</span><span class="sxs-lookup"><span data-stu-id="9a234-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="9a234-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a234-128">Remarks</span></span>

<span data-ttu-id="9a234-129">Это сообщение изменяет параметры числа строк, заданных элементом **CRowset** структуры [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , если таблица содержит несколько последовательных строк.</span><span class="sxs-lookup"><span data-stu-id="9a234-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="9a234-130">Если параметр **CRowset** меньше 0, сообщение перебирается до конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a234-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="9a234-131">Если число новых ячеек отличается от числа текущих ячеек на + 1 или 1, то вставляет или удаляет ячейку в индексе, указанном элементом **ицелл** элемента **таблеровпармс**.</span><span class="sxs-lookup"><span data-stu-id="9a234-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="9a234-132">Начальная строка таблицы определяется позицией символа.</span><span class="sxs-lookup"><span data-stu-id="9a234-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="9a234-133">Это расположение задается элементами **кпстартров** со значениями, которые больше или равны нулю.</span><span class="sxs-lookup"><span data-stu-id="9a234-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="9a234-134">Значение должно находиться внутри строки таблицы, но не внутри вложенной таблицы, если только вы не хотите изменить параметры таблицы s.</span><span class="sxs-lookup"><span data-stu-id="9a234-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="9a234-135">Если элемент **кпстартров** равен 1, то позиции символа присваивается текущий выделенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="9a234-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="9a234-136">Для этого разместите выделение в любом месте строки таблицы или выберите строку с активной конечной точки выделения в конце строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a234-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a234-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9a234-137">Requirements</span></span>



| <span data-ttu-id="9a234-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9a234-138">Requirement</span></span> | <span data-ttu-id="9a234-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9a234-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a234-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a234-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9a234-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9a234-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9a234-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a234-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9a234-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9a234-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a234-144">Header</span><span class="sxs-lookup"><span data-stu-id="9a234-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a234-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a234-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a234-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a234-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a234-147">**EM \_ жеттаблепармс**</span><span class="sxs-lookup"><span data-stu-id="9a234-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





