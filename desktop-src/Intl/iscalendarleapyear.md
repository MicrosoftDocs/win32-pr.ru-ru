---
description: Не рекомендуется. Определяет, является ли указанный год високосным годом в заданной эре для конкретного календаря.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Функция Искалендарлеапеар
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910108"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="46e85-104">Функция Искалендарлеапеар</span><span class="sxs-lookup"><span data-stu-id="46e85-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="46e85-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="46e85-105">Deprecated.</span></span> <span data-ttu-id="46e85-106">Определяет, является ли указанный год високосным годом в заданной эре для конкретного календаря.</span><span class="sxs-lookup"><span data-stu-id="46e85-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e85-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46e85-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="46e85-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46e85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e85-109">*Калид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46e85-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e85-110">[Идентификатор календаря](calendar-identifiers.md) , используемый для проверки високосного года.</span><span class="sxs-lookup"><span data-stu-id="46e85-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="46e85-111">*year (год* \[ ) окне\]</span><span class="sxs-lookup"><span data-stu-id="46e85-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e85-112">Год для проверки.</span><span class="sxs-lookup"><span data-stu-id="46e85-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="46e85-113">*эра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46e85-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e85-114">Эпоха для проверки.</span><span class="sxs-lookup"><span data-stu-id="46e85-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e85-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46e85-115">Return value</span></span>

<span data-ttu-id="46e85-116">Возвращает **значение true** , если указанный год является високосным годом, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46e85-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="46e85-117">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="46e85-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="46e85-118">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="46e85-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="46e85-119">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="46e85-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e85-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46e85-120">Remarks</span></span>

<span data-ttu-id="46e85-121">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="46e85-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="46e85-122">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="46e85-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="46e85-123">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и именем этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="46e85-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e85-124">Требования</span><span class="sxs-lookup"><span data-stu-id="46e85-124">Requirements</span></span>



| <span data-ttu-id="46e85-125">Требование</span><span class="sxs-lookup"><span data-stu-id="46e85-125">Requirement</span></span> | <span data-ttu-id="46e85-126">Значение</span><span class="sxs-lookup"><span data-stu-id="46e85-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e85-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46e85-127">Minimum supported client</span></span><br/> | <span data-ttu-id="46e85-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46e85-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46e85-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46e85-129">Minimum supported server</span></span><br/> | <span data-ttu-id="46e85-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46e85-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46e85-131">DLL</span><span class="sxs-lookup"><span data-stu-id="46e85-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e85-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46e85-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e85-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46e85-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e85-134">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="46e85-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="46e85-135">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="46e85-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
