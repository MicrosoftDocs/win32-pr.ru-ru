---
description: Структура FORM_INFO_1 содержит сведения о печатной форме. Эти сведения включают источник печатных форм, его имя, размеры и размеры области печати.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Структура FORM_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719570"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="df871-104">Структура FORM_INFO_1</span><span class="sxs-lookup"><span data-stu-id="df871-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="df871-105">Структура **FORM_INFO_1** содержит сведения о печатной форме.</span><span class="sxs-lookup"><span data-stu-id="df871-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="df871-106">Эти сведения включают источник формы печати, ее имя, размеры и размеры области печати.</span><span class="sxs-lookup"><span data-stu-id="df871-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="df871-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df871-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="df871-108">Члены</span><span class="sxs-lookup"><span data-stu-id="df871-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="df871-109">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="df871-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="df871-110">Свойства формы.</span><span class="sxs-lookup"><span data-stu-id="df871-110">The form properties.</span></span> <span data-ttu-id="df871-111">Определены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="df871-111">The following values are defined.</span></span>



| <span data-ttu-id="df871-112">Значение</span><span class="sxs-lookup"><span data-stu-id="df871-112">Value</span></span>         | <span data-ttu-id="df871-113">Значение</span><span class="sxs-lookup"><span data-stu-id="df871-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df871-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="df871-114">FORM_USER</span></span>    | <span data-ttu-id="df871-115">Если задан этот битовый флаг, форма была определена пользователем.</span><span class="sxs-lookup"><span data-stu-id="df871-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="df871-116">Формы с установленным флагом определяются в реестре.</span><span class="sxs-lookup"><span data-stu-id="df871-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="df871-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="df871-117">FORM_BUILTIN</span></span> | <span data-ttu-id="df871-118">Если этот флаг bit установлен, форма является частью диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="df871-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="df871-119">Определения форм с этим набором флагов не отображаются в реестре.</span><span class="sxs-lookup"><span data-stu-id="df871-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="df871-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="df871-120">FORM_PRINTER</span></span> | <span data-ttu-id="df871-121">Если этот битовый флаг установлен, форма связана с определенным принтером и его определение отображается в реестре.</span><span class="sxs-lookup"><span data-stu-id="df871-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="df871-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="df871-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="df871-123">Указатель на строку, завершающуюся нулем, которая указывает имя формы.</span><span class="sxs-lookup"><span data-stu-id="df871-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="df871-124">Длина имени формы не может превышать 31 символ.</span><span class="sxs-lookup"><span data-stu-id="df871-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="df871-125">**Размер**</span><span class="sxs-lookup"><span data-stu-id="df871-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="df871-126">Ширина и высота (в тысячах миллиметров) формы.</span><span class="sxs-lookup"><span data-stu-id="df871-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="df871-127">**имажеаблеареа**</span><span class="sxs-lookup"><span data-stu-id="df871-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="df871-128">Ширина и высота (в тысячах миллиметров) формы.</span><span class="sxs-lookup"><span data-stu-id="df871-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df871-129">Требования</span><span class="sxs-lookup"><span data-stu-id="df871-129">Requirements</span></span>



| <span data-ttu-id="df871-130">Требование</span><span class="sxs-lookup"><span data-stu-id="df871-130">Requirement</span></span> | <span data-ttu-id="df871-131">Значение</span><span class="sxs-lookup"><span data-stu-id="df871-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df871-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df871-132">Minimum supported client</span></span><br/> | <span data-ttu-id="df871-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df871-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df871-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df871-134">Minimum supported server</span></span><br/> | <span data-ttu-id="df871-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df871-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df871-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="df871-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="df871-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df871-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="df871-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="df871-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="df871-139">**_FORM_INFO_1W** (Юникод) и **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="df871-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="df871-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df871-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df871-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="df871-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="df871-142">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="df871-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="df871-143">**аддформ**</span><span class="sxs-lookup"><span data-stu-id="df871-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="df871-144">**Форма**</span><span class="sxs-lookup"><span data-stu-id="df871-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="df871-145">**сетформ**</span><span class="sxs-lookup"><span data-stu-id="df871-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




