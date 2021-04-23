---
title: Сообщение EM_GETTABLEPARMS (RichEdit. h)
description: Получает табличные параметры для строки таблицы и параметры ячейки для указанного числа ячеек.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Элементы управления Windows для EM_GETTABLEPARMS сообщений
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891834"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="91637-104">\_Сообщение ЖЕТТАБЛЕПАРМС EM</span><span class="sxs-lookup"><span data-stu-id="91637-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="91637-105">Получает табличные параметры для строки таблицы и параметры ячейки для указанного числа ячеек.</span><span class="sxs-lookup"><span data-stu-id="91637-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="91637-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91637-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91637-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91637-108">Указатель на структуру [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="91637-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="91637-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91637-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91637-110">Указатель на структуру [**таблецеллпармс**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="91637-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91637-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91637-111">Return value</span></span>

<span data-ttu-id="91637-112">\_При успешном выполнении или один из следующих кодов ошибок возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="91637-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="91637-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="91637-113">Return code</span></span>                                                                                    | <span data-ttu-id="91637-114">Описание</span><span class="sxs-lookup"><span data-stu-id="91637-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91637-115"><dt>**Д \_ Не пройден**</dt></span><span class="sxs-lookup"><span data-stu-id="91637-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="91637-116">Невозможно внести изменения.</span><span class="sxs-lookup"><span data-stu-id="91637-116">Changes cannot be made.</span></span> <span data-ttu-id="91637-117">Это может произойти, если элемент управления является обычным текстовым или однострочным или если точка вставки находится внутри математического объекта.</span><span class="sxs-lookup"><span data-stu-id="91637-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="91637-118">Это также происходит, если таблицы отключены, если в сообщении [**EM \_ сетедитстиликс**](em-seteditstyleex.md) задается значимое значение **SES \_ ex \_** .</span><span class="sxs-lookup"><span data-stu-id="91637-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="91637-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="91637-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="91637-120">Параметр *wParam* или *lParam* имеет значение null или указывает на недопустимую структуру.</span><span class="sxs-lookup"><span data-stu-id="91637-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="91637-121">Элемент **кбров** структуры [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) должен равняться `sizeof(TABLEROWPARMS)` или sizeof (таблеровпармс) 2 \* sizeof (Long).</span><span class="sxs-lookup"><span data-stu-id="91637-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="91637-122">Последнее значение — это размер структуры RichEdit 4,1 **таблеровпармс** .</span><span class="sxs-lookup"><span data-stu-id="91637-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="91637-123">Элемент **кбцелл** структуры **таблеровпармс** должен равняться `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="91637-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="91637-124">Значение позиции символа запроса должно находиться на разделителе строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="91637-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="91637-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="91637-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="91637-126">Недостаточно свободной памяти.</span><span class="sxs-lookup"><span data-stu-id="91637-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="91637-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91637-127">Remarks</span></span>

<span data-ttu-id="91637-128">Это сообщение получает табличные параметры для строки на позиции символа, заданной элементом **кпстартров** структуры [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , и количество ячеек, заданных элементом **кцеллс** структуры [**таблецеллпармс**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="91637-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="91637-129">Позицией символа, определяемой элементом **кпстартров** структуры [**таблеровпармс**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , должна быть в начале строки таблицы или в конце строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="91637-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="91637-130">Если **кпстартров** имеет значение 1, то позиции символа присваивается текущий выделенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="91637-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="91637-131">В этом случае разместите выделение в конце строки (между символом ячейки и концом разделителя строки таблицы) или выберите строку.</span><span class="sxs-lookup"><span data-stu-id="91637-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="91637-132">Требования</span><span class="sxs-lookup"><span data-stu-id="91637-132">Requirements</span></span>



| <span data-ttu-id="91637-133">Требование</span><span class="sxs-lookup"><span data-stu-id="91637-133">Requirement</span></span> | <span data-ttu-id="91637-134">Значение</span><span class="sxs-lookup"><span data-stu-id="91637-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91637-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91637-135">Minimum supported client</span></span><br/> | <span data-ttu-id="91637-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="91637-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="91637-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91637-137">Minimum supported server</span></span><br/> | <span data-ttu-id="91637-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="91637-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91637-139">Header</span><span class="sxs-lookup"><span data-stu-id="91637-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="91637-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="91637-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91637-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91637-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91637-142">**EM \_ сеттаблепармс**</span><span class="sxs-lookup"><span data-stu-id="91637-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





