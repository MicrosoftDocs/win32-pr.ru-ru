---
description: Не рекомендуется. Возвращает поддерживаемый диапазон дат для указанного календаря.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Функция Жеткалендарсуппортеддатеранже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998925"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="80e36-104">Функция Жеткалендарсуппортеддатеранже</span><span class="sxs-lookup"><span data-stu-id="80e36-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="80e36-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="80e36-105">Deprecated.</span></span> <span data-ttu-id="80e36-106">Возвращает поддерживаемый диапазон дат для указанного календаря.</span><span class="sxs-lookup"><span data-stu-id="80e36-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e36-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80e36-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="80e36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80e36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e36-109">*Календарь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80e36-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e36-110">[Идентификатор календаря](calendar-identifiers.md) , для которого требуется получить поддерживаемый диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="80e36-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="80e36-111">*лпкалминдатетиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80e36-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e36-112">Указатель на структуру [**калдатетиме**](caldatetime.md) , определяющую минимальную поддерживаемую дату.</span><span class="sxs-lookup"><span data-stu-id="80e36-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="80e36-113">*лпкалмаксдатетиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80e36-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e36-114">Указатель на структуру [**калдатетиме**](caldatetime.md) , определяющую максимальную поддерживаемую дату.</span><span class="sxs-lookup"><span data-stu-id="80e36-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e36-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80e36-115">Return value</span></span>

<span data-ttu-id="80e36-116">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="80e36-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="80e36-117">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="80e36-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="80e36-118">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="80e36-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="80e36-119">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="80e36-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e36-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80e36-120">Remarks</span></span>

<span data-ttu-id="80e36-121">Самая ранняя дата, поддерживаемая этой функцией, — 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="80e36-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="80e36-122">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="80e36-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="80e36-123">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="80e36-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="80e36-124">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="80e36-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e36-125">Требования</span><span class="sxs-lookup"><span data-stu-id="80e36-125">Requirements</span></span>



| <span data-ttu-id="80e36-126">Требование</span><span class="sxs-lookup"><span data-stu-id="80e36-126">Requirement</span></span> | <span data-ttu-id="80e36-127">Значение</span><span class="sxs-lookup"><span data-stu-id="80e36-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80e36-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80e36-128">Minimum supported client</span></span><br/> | <span data-ttu-id="80e36-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80e36-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="80e36-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80e36-130">Minimum supported server</span></span><br/> | <span data-ttu-id="80e36-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80e36-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80e36-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80e36-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e36-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e36-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e36-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80e36-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e36-135">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="80e36-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="80e36-136">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="80e36-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="80e36-137">NLS: пример API-интерфейсов на основе имен</span><span class="sxs-lookup"><span data-stu-id="80e36-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
