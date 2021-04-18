---
title: Структура STOWED_EXCEPTION_INFORMATION_V2
description: Содержит сведения об исключении заполнения.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 структуры отчеты об ошибках Windows
- PSTOWED_EXCEPTION_INFORMATION_V2 отчеты об ошибках Windows указателя на структуру
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701087"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="e0605-105">\_ \_ Структура сведений об исключении заполнения \_ v2</span><span class="sxs-lookup"><span data-stu-id="e0605-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="e0605-106">Содержит сведения об исключении заполнения.</span><span class="sxs-lookup"><span data-stu-id="e0605-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0605-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0605-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="e0605-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e0605-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0605-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="e0605-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-110">Тип: **[ **\_ \_ \_ заголовок сведений об исключении заполнения**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="e0605-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-111">Структура [**\_ \_ \_ заголовка сведений об исключении заполнения**](stowed-exception-information-header.md) , содержащая сведения для этой родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="e0605-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="e0605-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="e0605-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-113">Тип: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-114">Код [**HRESULT**](/windows/desktop/WinProg/windows-data-types) для исключения заполнения.</span><span class="sxs-lookup"><span data-stu-id="e0605-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="e0605-115">**ексцептионформ**</span><span class="sxs-lookup"><span data-stu-id="e0605-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-116">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-117">2-разрядное значение, идентифицирующее форму исключения.</span><span class="sxs-lookup"><span data-stu-id="e0605-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="e0605-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0605-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="e0605-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e0605-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="e0605-120"><dt>**Заполнения \_ \_ \_ Двоичные данные формы исключений**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e0605-121">Это значение указывает, что форма исключения является двоичной.</span><span class="sxs-lookup"><span data-stu-id="e0605-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="e0605-122"><dt>**Заполнения \_ \_ \_ Текст формы исключения**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="e0605-123">Это значение указывает, что в качестве исключения используется текст.</span><span class="sxs-lookup"><span data-stu-id="e0605-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e0605-124">**Tидентификатор**</span><span class="sxs-lookup"><span data-stu-id="e0605-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-125">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-126">30-разрядное значение, идентифицирующее поток, вызвавший исключение.</span><span class="sxs-lookup"><span data-stu-id="e0605-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="e0605-127">При сохранении значение перемещается вправо на 2 бита.</span><span class="sxs-lookup"><span data-stu-id="e0605-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="e0605-128">Чтобы преобразовать его обратно в допустимый идентификатор потока, сдвиньте значение влево на 2.</span><span class="sxs-lookup"><span data-stu-id="e0605-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="e0605-129">Пример:</span><span class="sxs-lookup"><span data-stu-id="e0605-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="e0605-130">(*безымянная структура*)</span><span class="sxs-lookup"><span data-stu-id="e0605-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e0605-131">Члены этой вложенной структуры являются допустимыми только в том случае, если для элемента **ексцептионформ** задано значение **заполнения в \_ \_ виде \_ двоичной формы исключений**.</span><span class="sxs-lookup"><span data-stu-id="e0605-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="e0605-132">**ексцептионаддресс**</span><span class="sxs-lookup"><span data-stu-id="e0605-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-133">Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-134">Указатель, содержащий адрес исключения.</span><span class="sxs-lookup"><span data-stu-id="e0605-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="e0605-135">**стакктрацевордсизе**</span><span class="sxs-lookup"><span data-stu-id="e0605-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-136">Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-137">Размер (в байтах) каждого слова в трассировке стека, на которое указывает элемент **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="e0605-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e0605-138">Это значение равно 4 для 32-разрядных платформ и 8 для 64-разрядных платформ.</span><span class="sxs-lookup"><span data-stu-id="e0605-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="e0605-139">**стакктрацевордс**</span><span class="sxs-lookup"><span data-stu-id="e0605-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-140">Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-141">Количество слов в трассировке стека, на которое указывает элемент **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="e0605-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e0605-142">Число слов равно числу элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="e0605-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e0605-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="e0605-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-144">Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-145">Указатель на блок памяти, содержащий трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="e0605-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e0605-146">(*безымянная структура*)</span><span class="sxs-lookup"><span data-stu-id="e0605-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e0605-147">Элемент этой вложенной структуры допустим только в том случае, если для элемента **ексцептионформ** задано значение **заполнения в \_ \_ виде \_ текста формы исключения**.</span><span class="sxs-lookup"><span data-stu-id="e0605-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="e0605-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="e0605-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-149">Тип: **[ **пвстр**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-150">Указатель на строку, завершающуюся нулем, которая содержит текст ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="e0605-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e0605-151">**нестедексцептионтипе**</span><span class="sxs-lookup"><span data-stu-id="e0605-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-152">Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-153">32-разрядное значение, указывающее тип объекта, на который указывает элемент **нестедексцептион** .</span><span class="sxs-lookup"><span data-stu-id="e0605-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="e0605-154">Определите значение с помощью этого макроса типа swap-Definition, который предполагается с прямым порядком байтов:</span><span class="sxs-lookup"><span data-stu-id="e0605-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="e0605-155">Ниже приведены некоторые общие определения типов.</span><span class="sxs-lookup"><span data-stu-id="e0605-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="e0605-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e0605-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="e0605-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e0605-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="e0605-158"><dt>**Заполнения \_ \_Вложенный \_ тип исключения \_ None**</dt> <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="e0605-159">Это значение указывает на отсутствие вложенного объекта исключения.</span><span class="sxs-lookup"><span data-stu-id="e0605-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="e0605-160"><dt>**Заполнения \_ \_Вложенный \_ тип исключения \_ Win32**</dt> <dt>заполнения \_ Exception \_ Nested \_ Type (' W32E ')</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="e0605-161">Это значение указывает, что элемент **нестедексцептион** указывает на объект [**\_ записи исключения**](/windows/desktop/api/winnt/ns-winnt-exception_record) .</span><span class="sxs-lookup"><span data-stu-id="e0605-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="e0605-162"><dt>**Заполнения \_ EXCEPTION Nested \_ \_ Type \_ заполнения**</dt> <dt>заполнения \_ \_ Nested \_ Type (' стов ')</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="e0605-163">Это значение указывает, что элемент **нестедексцептион** указывает на другой объект исключения заполнения.</span><span class="sxs-lookup"><span data-stu-id="e0605-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="e0605-164">Другим объектом исключения заполнения может быть объект **\_ сведений об исключении заполнения \_ \_ версии 2** или другая версия с допустимым **элементом заголовка** , то есть элементом **заголовка** , содержащим допустимый [**\_ \_ \_ заголовок сведений об исключении заполнения**](stowed-exception-information-header.md).</span><span class="sxs-lookup"><span data-stu-id="e0605-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="e0605-165"><dt>**Заполнения \_ ИСКЛЮЧЕНИЕ вложенного типа \_ \_ \_ CLR**</dt> заполнения Exception Nested Type <dt> \_ \_ \_ (' файле clr1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="e0605-166">Это значение указывает, что элемент **нестедексцептион** указывает на объект исключения "файле clr1".</span><span class="sxs-lookup"><span data-stu-id="e0605-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="e0605-167"><dt>**Заполнения \_ EXCEPTION Nested \_ \_ Type \_ Leo**</dt> <dt>заполнения \_ \_ Nested \_ Type (' LEO1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="e0605-168">Это значение указывает, что элемент **нестедексцептион** указывает на объект исключения языка.</span><span class="sxs-lookup"><span data-stu-id="e0605-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e0605-169">**нестедексцептион**</span><span class="sxs-lookup"><span data-stu-id="e0605-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="e0605-170">Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0605-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e0605-171">Указатель на тип вложенного исключения.</span><span class="sxs-lookup"><span data-stu-id="e0605-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="e0605-172">Тип объекта указывается членом **нестедексцептионтипе** .</span><span class="sxs-lookup"><span data-stu-id="e0605-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0605-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0605-173">Remarks</span></span>

<span data-ttu-id="e0605-174">**Заполнения \_ Заголовок сведений об ИСКЛЮЧЕНии \_ \_ v2** и заполнения в настоящее время не определен в заголовке, который является общедоступным, поэтому необходимо определить их в исходном коде, прежде чем использовать их. [**\_ \_ \_**](stowed-exception-information-header.md)</span><span class="sxs-lookup"><span data-stu-id="e0605-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="e0605-175">Структура **\_ \_ сведений об исключении \_ заполнения** версии 1 идентична этой структуре, за исключением того, что она не содержит членов **нестедексцептионтипе** и **нестедексцептион** .</span><span class="sxs-lookup"><span data-stu-id="e0605-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0605-176">Требования</span><span class="sxs-lookup"><span data-stu-id="e0605-176">Requirements</span></span>



| <span data-ttu-id="e0605-177">Требование</span><span class="sxs-lookup"><span data-stu-id="e0605-177">Requirement</span></span> | <span data-ttu-id="e0605-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e0605-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e0605-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0605-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e0605-180">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e0605-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0605-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0605-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e0605-182">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0605-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e0605-183">Header</span><span class="sxs-lookup"><span data-stu-id="e0605-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0605-184"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="e0605-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0605-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0605-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0605-186">**\_запись исключения**</span><span class="sxs-lookup"><span data-stu-id="e0605-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="e0605-187">**\_ \_ заголовок сведений об ИСКЛЮЧЕНии заполнения \_**</span><span class="sxs-lookup"><span data-stu-id="e0605-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

