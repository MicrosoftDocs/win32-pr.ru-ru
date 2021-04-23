---
description: Не рекомендуется. Возвращает день недели, соответствующий указанному дню, и заполняет элемент DayOfWeek в указанной структуре КАЛДАТЕТИМЕ этим значением.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Функция Упдатекалендардайофвик
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684609"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="e5615-104">Функция Упдатекалендардайофвик</span><span class="sxs-lookup"><span data-stu-id="e5615-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="e5615-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e5615-105">Deprecated.</span></span> <span data-ttu-id="e5615-106">Возвращает день недели, соответствующий указанному дню, и заполняет элемент **DayOfWeek** в указанной структуре [**калдатетиме**](caldatetime.md) этим значением.</span><span class="sxs-lookup"><span data-stu-id="e5615-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5615-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5615-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="e5615-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5615-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5615-109">*лпкалдатетиме* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e5615-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5615-110">Указатель на структуру [**калдатетиме**](caldatetime.md) , содержащую дату, для которой необходимо задать день недели.</span><span class="sxs-lookup"><span data-stu-id="e5615-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5615-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5615-111">Return value</span></span>

<span data-ttu-id="e5615-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e5615-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="e5615-113">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="e5615-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="e5615-114">\_Дата ошибки \_ за пределами \_ \_ диапазона.</span><span class="sxs-lookup"><span data-stu-id="e5615-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="e5615-115">Указанная дата находится за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="e5615-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="e5615-116">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="e5615-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="e5615-117">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="e5615-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5615-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5615-118">Remarks</span></span>

<span data-ttu-id="e5615-119">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="e5615-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="e5615-120">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="e5615-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="e5615-121">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и именем этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="e5615-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5615-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e5615-122">Requirements</span></span>



| <span data-ttu-id="e5615-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e5615-123">Requirement</span></span> | <span data-ttu-id="e5615-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e5615-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5615-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5615-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e5615-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5615-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e5615-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5615-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e5615-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5615-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5615-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e5615-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5615-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5615-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5615-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5615-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5615-132">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="e5615-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="e5615-133">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="e5615-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="e5615-134">**калдатетиме**</span><span class="sxs-lookup"><span data-stu-id="e5615-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
