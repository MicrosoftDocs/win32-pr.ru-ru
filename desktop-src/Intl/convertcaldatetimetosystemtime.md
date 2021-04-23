---
description: Не рекомендуется. Преобразует указанную структуру КАЛДАТЕТИМЕ в структуру SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Функция Конверткалдатетиметосистемтиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683526"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="dbdc5-104">Функция Конверткалдатетиметосистемтиме</span><span class="sxs-lookup"><span data-stu-id="dbdc5-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="dbdc5-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-105">Deprecated.</span></span> <span data-ttu-id="dbdc5-106">Преобразует указанную структуру [**калдатетиме**](caldatetime.md) в структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="dbdc5-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbdc5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbdc5-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="dbdc5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbdc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbdc5-109">*лпкалдатетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbdc5-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdc5-110">Указатель на структуру [**калдатетиме**](caldatetime.md) для преобразования.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="dbdc5-111">*лпсистиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbdc5-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdc5-112">Указатель на эквивалентную структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="dbdc5-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbdc5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbdc5-113">Return value</span></span>

<span data-ttu-id="dbdc5-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="dbdc5-115">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="dbdc5-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="dbdc5-116">\_Дата ошибки \_ за пределами \_ \_ диапазона.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="dbdc5-117">Указанная дата находится за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="dbdc5-118">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="dbdc5-119">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbdc5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbdc5-120">Remarks</span></span>

<span data-ttu-id="dbdc5-121">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="dbdc5-122">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="dbdc5-123">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbdc5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="dbdc5-124">Requirements</span></span>



| <span data-ttu-id="dbdc5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="dbdc5-125">Requirement</span></span> | <span data-ttu-id="dbdc5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="dbdc5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbdc5-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbdc5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dbdc5-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbdc5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dbdc5-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbdc5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dbdc5-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbdc5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbdc5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dbdc5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbdc5-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbdc5-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbdc5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbdc5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbdc5-134">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="dbdc5-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="dbdc5-135">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="dbdc5-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="dbdc5-136">Получение сведений о времени и дате</span><span class="sxs-lookup"><span data-stu-id="dbdc5-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
