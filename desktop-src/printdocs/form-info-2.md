---
description: Содержит сведения о локализуемых формах печати.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Структура FORM_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264332"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="c160c-103">\_Структура сведения о форме \_ 2</span><span class="sxs-lookup"><span data-stu-id="c160c-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="c160c-104">Содержит сведения о локализуемых формах печати.</span><span class="sxs-lookup"><span data-stu-id="c160c-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="c160c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c160c-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="c160c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c160c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c160c-107">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="c160c-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-108">Свойства формы.</span><span class="sxs-lookup"><span data-stu-id="c160c-108">The form properties.</span></span> <span data-ttu-id="c160c-109">Определены следующие значения, но можно задать только одно из них.</span><span class="sxs-lookup"><span data-stu-id="c160c-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="c160c-110">При возврате из **формы \_ сведений \_ 2** функцией- [**формой**](getform.md) или [**енумформс**](enumforms.md) **Флаги** устанавливаются в текущее значение в базе данных Forms.</span><span class="sxs-lookup"><span data-stu-id="c160c-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="c160c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c160c-111">Value</span></span>         | <span data-ttu-id="c160c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c160c-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c160c-113">\_пользователь формы</span><span class="sxs-lookup"><span data-stu-id="c160c-113">FORM\_USER</span></span>    | <span data-ttu-id="c160c-114">Если задан этот битовый флаг, форма была определена пользователем.</span><span class="sxs-lookup"><span data-stu-id="c160c-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="c160c-115">Формы с установленным флагом определяются в реестре.</span><span class="sxs-lookup"><span data-stu-id="c160c-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="c160c-116">\_Встроенная форма</span><span class="sxs-lookup"><span data-stu-id="c160c-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="c160c-117">Если этот флаг bit установлен, форма является частью диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="c160c-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="c160c-118">Определения форм с этим набором флагов не отображаются в реестре.</span><span class="sxs-lookup"><span data-stu-id="c160c-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="c160c-119">Встроенные формы не могут быть изменены, поэтому этот флаг не следует задавать при передаче структуры в [**аддформ**](addform.md) или [**сетформ**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="c160c-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="c160c-120">Форма \_ принтера</span><span class="sxs-lookup"><span data-stu-id="c160c-120">FORM\_PRINTER</span></span> | <span data-ttu-id="c160c-121">Если этот битовый флаг установлен, форма связана с определенным принтером и его определение отображается в реестре.</span><span class="sxs-lookup"><span data-stu-id="c160c-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="c160c-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="c160c-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-123">Указатель на строку, завершающуюся нулем, которая указывает имя формы.</span><span class="sxs-lookup"><span data-stu-id="c160c-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="c160c-124">Длина имени формы не может превышать 31 символ.</span><span class="sxs-lookup"><span data-stu-id="c160c-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-125">**Размер**</span><span class="sxs-lookup"><span data-stu-id="c160c-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-126">Ширина и высота формы в тысячах миллиметров.</span><span class="sxs-lookup"><span data-stu-id="c160c-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-127">**имажеаблеареа**</span><span class="sxs-lookup"><span data-stu-id="c160c-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-128">Ширина и высота в тысячах миллиметров области страницы, на которой принтер может печататься.</span><span class="sxs-lookup"><span data-stu-id="c160c-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-129">**пкэйворд**</span><span class="sxs-lookup"><span data-stu-id="c160c-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-130">Указатель на нелокализуемый строковый идентификатор формы.</span><span class="sxs-lookup"><span data-stu-id="c160c-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="c160c-131">При передаче в [**аддформ**](addform.md) или [**сетформ**](setform.md)это дает вызывающей стороне возможность идентифицировать форму во всех языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="c160c-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="c160c-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-133">Указывает способ получения локализованного отображаемого имени для формы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c160c-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="c160c-134">Определены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c160c-134">The following values are defined.</span></span> <span data-ttu-id="c160c-135">Только один из этих вызовов может быть установлен в [**аддформ**](addform.md) или [**сетформ**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="c160c-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="c160c-136">СТРОКИ \_ муидлл и String \_ лангпаир можно задать в **форме \_ info \_ 2** (s), возвращаемой функцией GetString [](getform.md) или [**енумформс**](enumforms.md).</span><span class="sxs-lookup"><span data-stu-id="c160c-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="c160c-137">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c160c-137">See Remarks.</span></span>



| <span data-ttu-id="c160c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c160c-138">Value</span></span>            | <span data-ttu-id="c160c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c160c-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c160c-140">Строка \_ None</span><span class="sxs-lookup"><span data-stu-id="c160c-140">STRING\_NONE</span></span>     | <span data-ttu-id="c160c-141">Локализованное отображаемое имя отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c160c-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="c160c-142">Строка \_ муидлл</span><span class="sxs-lookup"><span data-stu-id="c160c-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="c160c-143">Отображаемое имя извлекается из библиотеки DLL локализованных ресурсов [пользовательского интерфейса](/windows/desktop/Intl/mui-resource-management) , указанной в **пмуидлл**.</span><span class="sxs-lookup"><span data-stu-id="c160c-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="c160c-144">Идентификатор находится в элементе **двресаурцеид** .</span><span class="sxs-lookup"><span data-stu-id="c160c-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="c160c-145">Строка \_ лангпаир</span><span class="sxs-lookup"><span data-stu-id="c160c-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="c160c-146">Отображаемое имя и идентификатор языка предоставляются непосредственно в **пдисплайнаме** , а язык задается параметром **влангид**.</span><span class="sxs-lookup"><span data-stu-id="c160c-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="c160c-147">**пмуидлл**</span><span class="sxs-lookup"><span data-stu-id="c160c-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-148">Локализованная Библиотека ресурсов [многоязыкового интерфейса пользователя](/windows/desktop/Intl/mui-resource-management) , содержащая локализованное отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="c160c-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-149">**двресаурцеид**</span><span class="sxs-lookup"><span data-stu-id="c160c-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-150">Идентификатор ресурса отображаемого имени формы в **пмуидлл**.</span><span class="sxs-lookup"><span data-stu-id="c160c-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-151">**пдисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="c160c-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-152">Отображаемое имя формы на языке, указанном параметром **влангид**.</span><span class="sxs-lookup"><span data-stu-id="c160c-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-153">**влангид**</span><span class="sxs-lookup"><span data-stu-id="c160c-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-154">Язык **пдисплайнаме**.</span><span class="sxs-lookup"><span data-stu-id="c160c-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c160c-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c160c-155">Remarks</span></span>

<span data-ttu-id="c160c-156">При вызове [**аддформ**](addform.md) или [**сетформ**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="c160c-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="c160c-157">Если **стрингтипе** имеет значение String \_ None, то оба **пмуидлл** и **пдисплайнаме** должны быть **равны NULL** , а оба **двресаурцеид** и **влангид** должны быть равны 0.</span><span class="sxs-lookup"><span data-stu-id="c160c-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="c160c-158">Если **стрингтипе** имеет строковый \_ муидлл, **Пдисплайнаме** должен иметь **значение NULL** , а **влангид** должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="c160c-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="c160c-159">Если **стрингтипе** имеет строковый \_ лангпаир, **Пмуидлл** должен иметь **значение NULL** , а **двресаурцеид** должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="c160c-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="c160c-160">Для **формы \_ сведения \_ 2** , возвращенные вызовом функции [](getform.md) [**енумформс**](enumforms.md):</span><span class="sxs-lookup"><span data-stu-id="c160c-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="c160c-161">Если **стрингтипе** является строкой \_ муидлл и String \_ лангпаир, **пмуидлл**, **пдисплайнаме**, **двресаурцеид** и **влангид** , все они имеют допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="c160c-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="c160c-162">Если **стрингтипе** — \_ только String Муидлл, то **пмуидлл** и **двресаурцеид** будут иметь допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="c160c-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="c160c-163">**пдисплайнаме** будет иметь **значение NULL** , а **влангид** — 0.</span><span class="sxs-lookup"><span data-stu-id="c160c-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="c160c-164">Если **стрингтипе** — \_ только String Лангпаир, то **пдисплайнаме** и **влангид** будут иметь допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="c160c-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="c160c-165">**пмуидлл** будет иметь **значение NULL** , а **двресаурцеид** — 0.</span><span class="sxs-lookup"><span data-stu-id="c160c-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c160c-166">Требования</span><span class="sxs-lookup"><span data-stu-id="c160c-166">Requirements</span></span>



| <span data-ttu-id="c160c-167">Требование</span><span class="sxs-lookup"><span data-stu-id="c160c-167">Requirement</span></span> | <span data-ttu-id="c160c-168">Значение</span><span class="sxs-lookup"><span data-stu-id="c160c-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c160c-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c160c-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c160c-170">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c160c-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c160c-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c160c-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c160c-172">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c160c-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c160c-173">Header</span><span class="sxs-lookup"><span data-stu-id="c160c-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c160c-174"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c160c-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c160c-175">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c160c-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c160c-176">**\_ \_ Сведения о форме \_ 2W** (Юникод) и **\_ \_ сведения о форме \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c160c-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="c160c-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c160c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c160c-178">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="c160c-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c160c-179">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="c160c-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c160c-180">Многоязыковой интерфейс пользователя</span><span class="sxs-lookup"><span data-stu-id="c160c-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="c160c-181">**аддформ**</span><span class="sxs-lookup"><span data-stu-id="c160c-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="c160c-182">**Форма**</span><span class="sxs-lookup"><span data-stu-id="c160c-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="c160c-183">**енумформс**</span><span class="sxs-lookup"><span data-stu-id="c160c-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="c160c-184">**сетформ**</span><span class="sxs-lookup"><span data-stu-id="c160c-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

