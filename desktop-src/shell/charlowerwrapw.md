---
description: Преобразует строку символов в Юникоде или один символ в нижний регистр.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Функция Чарловерврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540559"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="8bd58-103">Функция Чарловерврапв</span><span class="sxs-lookup"><span data-stu-id="8bd58-103">CharLowerWrapW function</span></span>

<span data-ttu-id="8bd58-104">\[**Чарловерврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8bd58-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="8bd58-105">Она может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="8bd58-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="8bd58-106">На своем месте следует использовать [**чарловерв**](/windows/win32/api/winuser/nf-winuser-charlowera) .\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="8bd58-107">Преобразует строку символов в Юникоде или один символ в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="8bd58-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="8bd58-108">Если операнд является символьной строкой, функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="8bd58-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="8bd58-109">**Чарловерврапв** — это оболочка для функции **чарловерв** .</span><span class="sxs-lookup"><span data-stu-id="8bd58-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="8bd58-110">Дополнительные сведения об использовании см. на странице [**чарловер**](/windows/win32/api/winuser/nf-winuser-charlowera) .</span><span class="sxs-lookup"><span data-stu-id="8bd58-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8bd58-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bd58-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="8bd58-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bd58-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd58-113">*PCH* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd58-114">Тип: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8bd58-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="8bd58-115">Указатель на строку в Юникоде, заканчивающуюся нулем, или отдельный символ.</span><span class="sxs-lookup"><span data-stu-id="8bd58-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="8bd58-116">Если значение этого параметра в высоком алфавите равно нулю, то слово нижнего порядка должно содержать только один символ для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8bd58-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd58-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bd58-117">Return value</span></span>

<span data-ttu-id="8bd58-118">Тип: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8bd58-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="8bd58-119">Если *PCH* является символьной строкой, функция возвращает указатель на преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="8bd58-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="8bd58-120">Так как строка преобразуется на месте, возвращаемое значение равно *PCH*.</span><span class="sxs-lookup"><span data-stu-id="8bd58-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="8bd58-121">Если *PCH* является одиночным символом, то возвращаемое значение представляет собой 32-разрядное значение, в котором слово с высоким порядковым значением равно нулю, а слово низкого порядка содержит преобразованный символ.</span><span class="sxs-lookup"><span data-stu-id="8bd58-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="8bd58-122">Нет индикации об успешном или неудачном завершении.</span><span class="sxs-lookup"><span data-stu-id="8bd58-122">There is no indication of success or failure.</span></span> <span data-ttu-id="8bd58-123">Сбой является редким.</span><span class="sxs-lookup"><span data-stu-id="8bd58-123">Failure is rare.</span></span> <span data-ttu-id="8bd58-124">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8bd58-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd58-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bd58-125">Remarks</span></span>

<span data-ttu-id="8bd58-126">Предпочтительным методом является использование [**чарловерв**](/windows/win32/api/winuser/nf-winuser-charlowera) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="8bd58-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="8bd58-127">**Чарловерврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 38.</span><span class="sxs-lookup"><span data-stu-id="8bd58-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd58-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8bd58-128">Requirements</span></span>



| <span data-ttu-id="8bd58-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8bd58-129">Requirement</span></span> | <span data-ttu-id="8bd58-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8bd58-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd58-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bd58-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd58-132">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bd58-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bd58-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd58-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8bd58-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8bd58-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bd58-136"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="8bd58-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd58-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bd58-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd58-138">**чарловер**</span><span class="sxs-lookup"><span data-stu-id="8bd58-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
