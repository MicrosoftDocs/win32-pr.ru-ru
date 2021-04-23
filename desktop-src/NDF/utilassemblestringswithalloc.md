---
title: Функция Утилассемблестрингсвисаллок (Ндаттрибутилс. h)
description: Выделяет строку и форматирует ее с помощью строк, предоставленных таблицей строк. Эта функция использует Стрингкчпринтф для создания форматированной строки.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Утилассемблестрингсвисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804061"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="3e112-105">Функция Утилассемблестрингсвисаллок</span><span class="sxs-lookup"><span data-stu-id="3e112-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="3e112-106">Функция **утилассемблестрингсвисаллок** выделяет строку и форматирует ее с помощью строк, предоставленных таблицей строк.</span><span class="sxs-lookup"><span data-stu-id="3e112-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="3e112-107">Эта функция использует [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) для создания форматированной строки.</span><span class="sxs-lookup"><span data-stu-id="3e112-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e112-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e112-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="3e112-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e112-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e112-110">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e112-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-111">Введите: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="3e112-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="3e112-112">Расположение, в которое будет помещена вновь выделенная строка.</span><span class="sxs-lookup"><span data-stu-id="3e112-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="3e112-113">Если строка больше не нужна, она должна быть освобождена с помощью [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3e112-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="3e112-114">*Буффермакс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e112-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-115">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3e112-115">Type: **UINT**</span></span>

<span data-ttu-id="3e112-116">Максимально допустимое число символов в строке, выделенной *буфером*.</span><span class="sxs-lookup"><span data-stu-id="3e112-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="3e112-117">Если полученная Форматированная строка длиннее, чем указанное число символов, она усекается и завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="3e112-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="3e112-118">Этот параметр не может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3e112-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e112-119">*Инпутформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e112-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-120">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="3e112-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3e112-121">Строковый ресурс из таблицы строк, представляющей параметр формата, переданный в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span><span class="sxs-lookup"><span data-stu-id="3e112-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="3e112-122">Он создается с помощью [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="3e112-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="3e112-123">Формат строки ресурса должен указывать либо параметр формата, принимающий расширенную строку, либо параметр формата, исключая длинную строку без знака и широкие строки.</span><span class="sxs-lookup"><span data-stu-id="3e112-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="3e112-124">*InputString* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e112-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-125">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="3e112-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3e112-126">Строковый ресурс из таблицы строк, представляющей аргумент, передаваемый в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) вместо широкой строки в параметре format.</span><span class="sxs-lookup"><span data-stu-id="3e112-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="3e112-127">Он создается с помощью [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="3e112-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="3e112-128">*Аддитионаларгумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e112-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-129">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3e112-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="3e112-130">Значение true, если *аддитионалвалуе* следует передать в качестве первого аргумента форматирования в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); в противном случае передается значение false (и будет передана только строка ресурса, определенная *InputString* ).</span><span class="sxs-lookup"><span data-stu-id="3e112-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="3e112-131">*Аддитионалвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e112-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e112-132">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="3e112-132">Type: **ULONG**</span></span>

<span data-ttu-id="3e112-133">Значение, которое передается в качестве первого аргумента форматирования в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) , если *аддитионаларгумент* имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3e112-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e112-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e112-134">Return value</span></span>

<span data-ttu-id="3e112-135">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3e112-135">Type: **HRESULT**</span></span>

<span data-ttu-id="3e112-136">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="3e112-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3e112-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3e112-137">Return code</span></span>                                                                                  | <span data-ttu-id="3e112-138">Описание</span><span class="sxs-lookup"><span data-stu-id="3e112-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e112-139"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3e112-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3e112-140">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="3e112-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="3e112-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e112-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3e112-142">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="3e112-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e112-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3e112-143">Requirements</span></span>



| <span data-ttu-id="3e112-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3e112-144">Requirement</span></span> | <span data-ttu-id="3e112-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3e112-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e112-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e112-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3e112-147">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e112-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e112-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e112-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3e112-149">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e112-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e112-150">Header</span><span class="sxs-lookup"><span data-stu-id="3e112-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e112-151"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e112-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e112-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e112-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e112-153">**утилстрингкопивисаллок**</span><span class="sxs-lookup"><span data-stu-id="3e112-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="3e112-154">**утиллоадстрингвисаллок**</span><span class="sxs-lookup"><span data-stu-id="3e112-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="3e112-155">**стрингкчпринтф**</span><span class="sxs-lookup"><span data-stu-id="3e112-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="3e112-156">**макеинтресаурце**</span><span class="sxs-lookup"><span data-stu-id="3e112-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="3e112-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="3e112-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

