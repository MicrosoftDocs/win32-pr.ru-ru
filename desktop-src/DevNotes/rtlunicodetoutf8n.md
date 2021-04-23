---
description: Преобразует указанную строку Юникода в новую символьную строку, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Функция RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141251"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="bb193-103">Функция RtlUnicodeToUTF8N</span><span class="sxs-lookup"><span data-stu-id="bb193-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="bb193-104">Преобразует указанную строку Юникода в новую символьную строку, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="bb193-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb193-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb193-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="bb193-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb193-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb193-107">*UTF8StringDestination* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb193-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb193-108">Указатель на выделенный вызывающим объектом буфер для получения переведенной строки.</span><span class="sxs-lookup"><span data-stu-id="bb193-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="bb193-109">*UTF8StringMaxByteCount* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb193-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb193-110">Максимальное число байтов, записываемых в *UTF8StringDestination*.</span><span class="sxs-lookup"><span data-stu-id="bb193-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="bb193-111">Если это значение приводит к усечению переведенной строки, **RtlUnicodeToUTF8N** возвращает состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="bb193-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="bb193-112">*UTF8StringActualByteCount* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="bb193-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bb193-113">Указатель на переменную, выделенную вызывающим объектом, которая получает длину переведенной строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="bb193-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="bb193-114">Этот параметр является необязательным и может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb193-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="bb193-115">Если строка усекается, возвращаемое число подсчитывает фактическое число усеченных строк.</span><span class="sxs-lookup"><span data-stu-id="bb193-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="bb193-116">*Уникодестрингсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb193-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb193-117">Указатель на строку источника Юникода для перевода.</span><span class="sxs-lookup"><span data-stu-id="bb193-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="bb193-118">\* Уникодестрингбитекаунт \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="bb193-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb193-119">Указывает число байтов в исходной строке Юникода, на которое указывает параметр *уникодестрингсаурце* .</span><span class="sxs-lookup"><span data-stu-id="bb193-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb193-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb193-120">Return value</span></span>

<span data-ttu-id="bb193-121">**RtlUnicodeToUTF8N** возвращает одно из следующих значений NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="bb193-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="bb193-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bb193-122">Return code</span></span>                                                                                                  | <span data-ttu-id="bb193-123">Описание</span><span class="sxs-lookup"><span data-stu-id="bb193-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb193-124"><dt>**СОСТОЯНИЕ " \_ успешно"**</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="bb193-125">Строка Юникода была преобразована в UTF-8.</span><span class="sxs-lookup"><span data-stu-id="bb193-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="bb193-126"><dt>**СОСТОЯНИЕ \_ \_ \_ несопоставленных**</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="bb193-127">Обнаружен и заменен Недопустимый входной символ.</span><span class="sxs-lookup"><span data-stu-id="bb193-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="bb193-128">Это состояние считается состоянием успеха.</span><span class="sxs-lookup"><span data-stu-id="bb193-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="bb193-129"><dt>**\_Недопустимый \_ параметр Status**</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="bb193-130">Оба указателя на *UTF8StringDestination* и *UTF8StringActualByteCount* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb193-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="bb193-131"><dt>**СОСТОЯНИЕ " \_ Недопустимый \_ параметр \_ 4"**</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="bb193-132">*Уникодестрингсаурце* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb193-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="bb193-133"><dt>**\_БУФЕР состояния \_ слишком \_ мал**</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="bb193-134">*UTF8StringDestination* был усечен.</span><span class="sxs-lookup"><span data-stu-id="bb193-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="bb193-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb193-135">Remarks</span></span>

<span data-ttu-id="bb193-136">Хотя *UTF8StringActualByteCount* является необязательным и может иметь **значение NULL**, вызывающие объекты должны предоставлять для него хранилище, так как полученная длина может использоваться для определения успешности преобразования.</span><span class="sxs-lookup"><span data-stu-id="bb193-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="bb193-137">Эта подпрограммы не изменяет исходную строку.</span><span class="sxs-lookup"><span data-stu-id="bb193-137">This routine does not modify the source string.</span></span> <span data-ttu-id="bb193-138">Он возвращает строку в кодировке UTF-8, завершающуюся нулем, если заданный *уникодестрингсаурце* включает завершающий нуль, а если заданный *UTF8StringMaxByteCount* не вызвал усечение.</span><span class="sxs-lookup"><span data-stu-id="bb193-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="bb193-139">Если выходные данные усекаются и обнаружен недопустимый входной символ, функция возвращает буфер состояния, что \_ \_ Ошибка слишком \_ мала.</span><span class="sxs-lookup"><span data-stu-id="bb193-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="bb193-140">Если *UTF8StringDestination* имеет значение **null** , функция возвратит требуемое число байтов для размещения переведенной строки без усечения в *UTF8StringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="bb193-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="bb193-141">Вызывающие объекты **RtlUnicodeToUTF8N** должны выполняться на уровне подготовки к уровню IRQL < \_ .</span><span class="sxs-lookup"><span data-stu-id="bb193-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb193-142">Требования</span><span class="sxs-lookup"><span data-stu-id="bb193-142">Requirements</span></span>



| <span data-ttu-id="bb193-143">Требование</span><span class="sxs-lookup"><span data-stu-id="bb193-143">Requirement</span></span> | <span data-ttu-id="bb193-144">Значение</span><span class="sxs-lookup"><span data-stu-id="bb193-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb193-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb193-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bb193-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb193-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bb193-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb193-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bb193-148">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb193-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bb193-149">Header</span><span class="sxs-lookup"><span data-stu-id="bb193-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb193-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="bb193-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bb193-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb193-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb193-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb193-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb193-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb193-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="bb193-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




