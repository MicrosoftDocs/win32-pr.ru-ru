---
description: Функция Жеткаптурекомментфромфиленаме извлекает комментарий записи из файла записи.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Функция Жеткаптурекомментфромфиленаме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673189"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="9c817-103">Функция Жеткаптурекомментфромфиленаме</span><span class="sxs-lookup"><span data-stu-id="9c817-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="9c817-104">Функция **жеткаптурекомментфромфиленаме** извлекает комментарий записи из [*файла записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="9c817-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c817-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c817-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="9c817-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c817-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c817-107">*лпфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c817-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c817-108">Указатель на имя файла записи.</span><span class="sxs-lookup"><span data-stu-id="9c817-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="9c817-109">*лпкоммент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c817-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c817-110">Указатель на предварительно выделенную строку комментария.</span><span class="sxs-lookup"><span data-stu-id="9c817-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="9c817-111">*BufferSize* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c817-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c817-112">Размер строки.</span><span class="sxs-lookup"><span data-stu-id="9c817-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c817-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c817-113">Return value</span></span>

<span data-ttu-id="9c817-114">Если функция выполнена успешно (т. е. Если комментарий найден и скопирован или в файле записи нет комментариев), возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9c817-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9c817-115">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c817-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="9c817-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c817-116">Return code</span></span>                                                                                                 | <span data-ttu-id="9c817-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9c817-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c817-118"><dt>**\_ \_ Ошибка чтения файла \_ нмерр**</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="9c817-119">Не удается прочитать комментарий записи.</span><span class="sxs-lookup"><span data-stu-id="9c817-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="9c817-120"><dt>**НМЕРР \_ Недопустимый \_ \_ Формат файла**</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="9c817-121">Кадр комментария имеет недопустимый формат файла.</span><span class="sxs-lookup"><span data-stu-id="9c817-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="9c817-122"><dt>**\_файл нмерр \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="9c817-123">Не удается найти файл, указанный параметром *лпфиленаме* .</span><span class="sxs-lookup"><span data-stu-id="9c817-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="9c817-124"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="9c817-125">Один из параметров указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="9c817-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="9c817-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c817-126">Remarks</span></span>

<span data-ttu-id="9c817-127">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптурекомментфромфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="9c817-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="9c817-128">Чтобы получить комментарий записи в режиме реального времени, вызовите функцию [жеткаптурекоммент](getcapturecomment.md) .</span><span class="sxs-lookup"><span data-stu-id="9c817-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c817-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9c817-129">Requirements</span></span>



| <span data-ttu-id="9c817-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9c817-130">Requirement</span></span> | <span data-ttu-id="9c817-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9c817-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c817-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c817-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9c817-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c817-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9c817-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c817-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9c817-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c817-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c817-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c817-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c817-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9c817-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c817-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c817-139"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c817-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9c817-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c817-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c817-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c817-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c817-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c817-143">жеткаптурекоммент</span><span class="sxs-lookup"><span data-stu-id="9c817-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




