---
title: Сообщение TB_ADDSTRING (Коммктрл. h)
description: Добавляет новую строку в пул строк панели инструментов.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Элементы управления Windows для TB_ADDSTRING сообщений
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654721"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="074c3-104">\_Сообщение ADDSTRING ТБ</span><span class="sxs-lookup"><span data-stu-id="074c3-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="074c3-105">Добавляет новую строку в пул строк панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="074c3-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="074c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="074c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="074c3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="074c3-108">Обработайте экземпляр модуля с исполняемым файлом, содержащим строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="074c3-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="074c3-109">Если аргумент *lParam* указывает на массив символов с одной или несколькими строками, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="074c3-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="074c3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="074c3-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="074c3-111">Идентификатор ресурса для строкового ресурса или указатель на массив TCHAR.</span><span class="sxs-lookup"><span data-stu-id="074c3-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="074c3-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="074c3-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074c3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="074c3-113">Return value</span></span>

<span data-ttu-id="074c3-114">Возвращает индекс первой новой строки, если успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="074c3-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="074c3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="074c3-115">Remarks</span></span>

<span data-ttu-id="074c3-116">Если параметр *wParam* имеет **значение NULL**, *lParam* указывает на массив символов с одной или несколькими строками, заканчивающимися нулем.</span><span class="sxs-lookup"><span data-stu-id="074c3-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="074c3-117">Последняя строка в массиве должна завершаться двумя символами NULL.</span><span class="sxs-lookup"><span data-stu-id="074c3-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="074c3-118">Если параметр *wParam* является HINSTANCE приложения или другого модуля, содержащего строковый ресурс, то параметр *lParam* представляет собой идентификатор ресурса строки.</span><span class="sxs-lookup"><span data-stu-id="074c3-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="074c3-119">Каждый элемент в строке должен начинаться с произвольного разделителя, а строка должна заканчиваться двумя такими символами.</span><span class="sxs-lookup"><span data-stu-id="074c3-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="074c3-120">Например, текст для трех кнопок может отображаться в таблице строк как «/Нев/опен/Саве//».</span><span class="sxs-lookup"><span data-stu-id="074c3-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="074c3-121">Сообщение возвращает индекс "New" в пуле строк панели инструментов, а остальные элементы находятся в последовательных позициях.</span><span class="sxs-lookup"><span data-stu-id="074c3-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="074c3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="074c3-122">Requirements</span></span>



| <span data-ttu-id="074c3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="074c3-123">Requirement</span></span> | <span data-ttu-id="074c3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="074c3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="074c3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="074c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="074c3-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="074c3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="074c3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="074c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="074c3-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="074c3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="074c3-129">Header</span><span class="sxs-lookup"><span data-stu-id="074c3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="074c3-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="074c3-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="074c3-131">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="074c3-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="074c3-132">**ТБ \_ АДДСТРИНГВ** (Юникод) и **ТБ \_ аддстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="074c3-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





