---
title: Структура АКЦЕЛТАБЛИНТРИ
description: Описывает данные в отдельном ресурсе таблицы сочетаний клавиш. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Меню структуры АКЦЕЛТАБЛИНТРИ и другие ресурсы
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492975"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="d7adc-105">Структура АКЦЕЛТАБЛИНТРИ</span><span class="sxs-lookup"><span data-stu-id="d7adc-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="d7adc-106">Описывает данные в отдельном ресурсе таблицы сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="d7adc-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="d7adc-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="d7adc-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7adc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7adc-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="d7adc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d7adc-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7adc-110">**ффлагс**</span><span class="sxs-lookup"><span data-stu-id="d7adc-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d7adc-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d7adc-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d7adc-112">Описание характеристик сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="d7adc-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="d7adc-113">Этот элемент может иметь одно или несколько из следующих значений из файла Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="d7adc-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="d7adc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d7adc-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="d7adc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7adc-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="d7adc-116"><dt>**фвирткэй**</dt> <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="d7adc-117">Сочетание клавиш — это [код виртуального ключа](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="d7adc-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="d7adc-118">Если этот флаг не указан, то предполагается, что клавиша быстрого вызова указывает код символа ASCII.</span><span class="sxs-lookup"><span data-stu-id="d7adc-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="d7adc-119"><dt>**Фноинверт**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="d7adc-120">При использовании сочетания клавиш пункт меню в строке меню не выделяется.</span><span class="sxs-lookup"><span data-stu-id="d7adc-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="d7adc-121">Этот атрибут устарел и хранится только для обеспечения обратной совместимости с файлами ресурсов, предназначенными для 16-разрядных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="d7adc-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="d7adc-122"><dt>**Фшифт**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="d7adc-123">Ускоритель активируется только в том случае, если пользователь нажмет клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d7adc-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="d7adc-124">Этот флаг применяется только к виртуальным ключам.</span><span class="sxs-lookup"><span data-stu-id="d7adc-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="d7adc-125"><dt>**Фконтрол**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="d7adc-126">Ускоритель активируется, только если пользователь нажимает клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="d7adc-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="d7adc-127">Этот флаг применяется только к виртуальным ключам.</span><span class="sxs-lookup"><span data-stu-id="d7adc-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="d7adc-128"><dt>**ФАЛТ**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="d7adc-129">Ускоритель активируется только в том случае, если пользователь нажмет клавишу ALT.</span><span class="sxs-lookup"><span data-stu-id="d7adc-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="d7adc-130">Этот флаг применяется только к виртуальным ключам.</span><span class="sxs-lookup"><span data-stu-id="d7adc-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="d7adc-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="d7adc-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="d7adc-132">Запись является последней в таблице сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="d7adc-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="d7adc-133">**ванси**</span><span class="sxs-lookup"><span data-stu-id="d7adc-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="d7adc-134">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d7adc-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d7adc-135">Значение символа ANSI или код виртуального ключа, который определяет сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="d7adc-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="d7adc-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="d7adc-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="d7adc-137">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d7adc-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d7adc-138">Идентификатор для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="d7adc-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="d7adc-139">Это значение, передаваемое в процедуру окна, когда пользователь нажимает указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="d7adc-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="d7adc-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="d7adc-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="d7adc-141">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d7adc-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d7adc-142">Число вставленных байтов, обеспечивающих согласованность структуры по границе **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d7adc-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7adc-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7adc-143">Remarks</span></span>

<span data-ttu-id="d7adc-144">Структура **акцелтаблинтри** повторяется для всех записей таблицы сочетаний клавиш в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="d7adc-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="d7adc-145">Последняя запись в таблице помечается значением 0x0080.</span><span class="sxs-lookup"><span data-stu-id="d7adc-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="d7adc-146">Количество элементов в таблице можно вычислить, если длина ресурса делится на восемь.</span><span class="sxs-lookup"><span data-stu-id="d7adc-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="d7adc-147">Затем приложение может случайно получить доступ к отдельным записям фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="d7adc-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7adc-148">Требования</span><span class="sxs-lookup"><span data-stu-id="d7adc-148">Requirements</span></span>



| <span data-ttu-id="d7adc-149">Требование</span><span class="sxs-lookup"><span data-stu-id="d7adc-149">Requirement</span></span> | <span data-ttu-id="d7adc-150">Значение</span><span class="sxs-lookup"><span data-stu-id="d7adc-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d7adc-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7adc-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d7adc-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7adc-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7adc-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7adc-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d7adc-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7adc-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d7adc-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7adc-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7adc-156">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d7adc-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7adc-157">**креатеакцелератортабле**</span><span class="sxs-lookup"><span data-stu-id="d7adc-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="d7adc-158">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d7adc-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7adc-159">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="d7adc-159">Resources</span></span>](resources.md)
</dt> </dl>

 

