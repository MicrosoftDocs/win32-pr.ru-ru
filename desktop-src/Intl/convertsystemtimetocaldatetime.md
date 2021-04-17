---
description: Не рекомендуется. Преобразует указанную структуру SYSTEMTIME в структуру КАЛДАТЕТИМЕ.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Функция Конвертсистемтиметокалдатетиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650822"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="4b829-104">Функция Конвертсистемтиметокалдатетиме</span><span class="sxs-lookup"><span data-stu-id="4b829-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="4b829-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4b829-105">Deprecated.</span></span> <span data-ttu-id="4b829-106">Преобразует указанную структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) в структуру [**калдатетиме**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="4b829-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b829-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b829-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="4b829-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b829-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b829-109">*лпсистиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b829-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b829-110">Указатель на структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) для преобразования.</span><span class="sxs-lookup"><span data-stu-id="4b829-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="4b829-111">*Калид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b829-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b829-112">Идентификатор системного [календаря](calendar-identifiers.md) , используемый при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="4b829-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b829-113">*лпкалдатетиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b829-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b829-114">Указатель на эквивалентную структуру [**калдатетиме**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="4b829-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b829-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b829-115">Return value</span></span>

<span data-ttu-id="4b829-116">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4b829-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="4b829-117">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="4b829-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4b829-118">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="4b829-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4b829-119">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4b829-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b829-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b829-120">Remarks</span></span>

<span data-ttu-id="4b829-121">Самая ранняя дата, поддерживаемая этой функцией, — 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="4b829-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="4b829-122">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4b829-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="4b829-123">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="4b829-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="4b829-124">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="4b829-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b829-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4b829-125">Requirements</span></span>



| <span data-ttu-id="4b829-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4b829-126">Requirement</span></span> | <span data-ttu-id="4b829-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4b829-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b829-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b829-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b829-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b829-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b829-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b829-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b829-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b829-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b829-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4b829-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b829-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b829-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b829-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b829-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b829-135">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="4b829-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4b829-136">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="4b829-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4b829-137">Получение сведений о времени и дате</span><span class="sxs-lookup"><span data-stu-id="4b829-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
