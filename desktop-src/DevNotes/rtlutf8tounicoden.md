---
description: Преобразует указанную исходную строку в строку в Юникоде, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Функция RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262578"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="e956f-103">Функция RtlUTF8ToUnicodeN</span><span class="sxs-lookup"><span data-stu-id="e956f-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="e956f-104">Преобразует указанную исходную строку в строку в Юникоде, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="e956f-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="e956f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e956f-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="e956f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e956f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e956f-107">*Уникодестрингдестинатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e956f-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e956f-108">Указатель на выделенный вызывающим объектом буфер, который получает переведенную строку.</span><span class="sxs-lookup"><span data-stu-id="e956f-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="e956f-109">*Уникодестрингмаксбитекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e956f-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e956f-110">Максимальное число байтов, которое должно быть записано на *уникодестрингдестинатион*.</span><span class="sxs-lookup"><span data-stu-id="e956f-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="e956f-111">Если это значение приводит к усечению переведенной строки, **RtlUTF8ToUnicodeN** возвращает состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="e956f-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="e956f-112">*Уникодестрингактуалбитекаунт* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e956f-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e956f-113">Указатель на переменную, выделенную вызывающим объектом, которая получает длину переведенной строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="e956f-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="e956f-114">Этот параметр является необязательным и может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e956f-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="e956f-115">Если строка усекается, возвращаемое число подсчитывает фактическое число усеченных строк.</span><span class="sxs-lookup"><span data-stu-id="e956f-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="e956f-116">*UTF8StringSource* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e956f-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e956f-117">Указатель на строку для перевода.</span><span class="sxs-lookup"><span data-stu-id="e956f-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="e956f-118">*UTF8StringByteCount* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e956f-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e956f-119">Размер строки в байтах в *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="e956f-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e956f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e956f-120">Return value</span></span>

<span data-ttu-id="e956f-121">**RtlUTF8ToUnicodeN** возвращает одно из следующих значений NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="e956f-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="e956f-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e956f-122">Return code</span></span>                                                                                                  | <span data-ttu-id="e956f-123">Описание</span><span class="sxs-lookup"><span data-stu-id="e956f-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e956f-124"><dt>**СОСТОЯНИЕ " \_ успешно"**</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="e956f-125">Строка преобразована в Юникод.</span><span class="sxs-lookup"><span data-stu-id="e956f-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="e956f-126"><dt>**СОСТОЯНИЕ \_ \_ \_ несопоставленных**</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="e956f-127">Обнаружен и заменен Недопустимый входной символ.</span><span class="sxs-lookup"><span data-stu-id="e956f-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="e956f-128">Это состояние считается состоянием успеха.</span><span class="sxs-lookup"><span data-stu-id="e956f-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="e956f-129"><dt>**\_Недопустимый \_ параметр Status**</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="e956f-130">Оба указателя на *уникодестрингдестинатион* и *Уникодестрингактуалбитекаунт* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e956f-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="e956f-131"><dt>**СОСТОЯНИЕ " \_ Недопустимый \_ параметр \_ 4"**</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="e956f-132">*UTF8StringSource* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e956f-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="e956f-133"><dt>**\_БУФЕР состояния \_ слишком \_ мал**</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="e956f-134">*Уникодестрингдестинатион* был усечен.</span><span class="sxs-lookup"><span data-stu-id="e956f-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e956f-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e956f-135">Remarks</span></span>

<span data-ttu-id="e956f-136">Хотя *уникодестрингактуалбитекаунт* является необязательным и может иметь **значение NULL**, вызывающие объекты должны предоставлять для него хранилище, так как полученная длина может использоваться для определения успешности преобразования.</span><span class="sxs-lookup"><span data-stu-id="e956f-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="e956f-137">Если выходные данные усекаются и обнаружен недопустимый входной символ, функция возвращает буфер состояния, что \_ \_ Ошибка слишком \_ мала.</span><span class="sxs-lookup"><span data-stu-id="e956f-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="e956f-138">Если *уникодестрингдестинатион* имеет значение **null** , функция возвратит требуемое число байтов для размещения переведенной строки без усечения в *уникодестрингактуалбитекаунт*.</span><span class="sxs-lookup"><span data-stu-id="e956f-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="e956f-139">**RtlUTF8ToUnicodeN** не изменяет исходную строку, если только указатели *уникодестрингдестинатион* и *UTF8StringSource* не эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="e956f-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="e956f-140">Возвращенная строка Юникода не оканчивается нулем.</span><span class="sxs-lookup"><span data-stu-id="e956f-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="e956f-141">Вызывающие объекты **RtlUTF8ToUnicodeN** должны выполняться на уровне подготовки к уровню IRQL < \_ .</span><span class="sxs-lookup"><span data-stu-id="e956f-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e956f-142">Требования</span><span class="sxs-lookup"><span data-stu-id="e956f-142">Requirements</span></span>



| <span data-ttu-id="e956f-143">Требование</span><span class="sxs-lookup"><span data-stu-id="e956f-143">Requirement</span></span> | <span data-ttu-id="e956f-144">Значение</span><span class="sxs-lookup"><span data-stu-id="e956f-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e956f-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e956f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e956f-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e956f-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e956f-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e956f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e956f-148">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e956f-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e956f-149">Header</span><span class="sxs-lookup"><span data-stu-id="e956f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e956f-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="e956f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e956f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e956f-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e956f-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e956f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e956f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e956f-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="e956f-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




