---
description: Не рекомендуется. Корректирует дату на указанное число лет, месяцев, недель или дней.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Функция Аджусткалендардате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682635"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="2cf98-104">Функция Аджусткалендардате</span><span class="sxs-lookup"><span data-stu-id="2cf98-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="2cf98-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2cf98-105">Deprecated.</span></span> <span data-ttu-id="2cf98-106">Корректирует дату на указанное число лет, месяцев, недель или дней.</span><span class="sxs-lookup"><span data-stu-id="2cf98-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf98-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cf98-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="2cf98-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cf98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf98-109">*лпкалдатетиме* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2cf98-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf98-110">Указатель на структуру [**калдатетиме**](caldatetime.md) , которая содержит дату и сведения о календаре для корректировки.</span><span class="sxs-lookup"><span data-stu-id="2cf98-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="2cf98-111">*калунит* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cf98-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf98-112">Значение перечисления [**калдатетиме \_ датеунит**](caldatetime-dateunit.md) , указывающее единицу даты, например дайунит.</span><span class="sxs-lookup"><span data-stu-id="2cf98-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="2cf98-113">*Сумма* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2cf98-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf98-114">Величина, на которую нужно скорректировать указанную дату.</span><span class="sxs-lookup"><span data-stu-id="2cf98-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf98-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cf98-115">Return value</span></span>

<span data-ttu-id="2cf98-116">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2cf98-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="2cf98-117">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="2cf98-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="2cf98-118">\_Дата ошибки \_ за пределами \_ \_ диапазона.</span><span class="sxs-lookup"><span data-stu-id="2cf98-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="2cf98-119">Указанная дата находится за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="2cf98-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="2cf98-120">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="2cf98-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="2cf98-121">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2cf98-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf98-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cf98-122">Remarks</span></span>

<span data-ttu-id="2cf98-123">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2cf98-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="2cf98-124">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="2cf98-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="2cf98-125">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="2cf98-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf98-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2cf98-126">Requirements</span></span>



| <span data-ttu-id="2cf98-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2cf98-127">Requirement</span></span> | <span data-ttu-id="2cf98-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2cf98-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf98-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cf98-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf98-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cf98-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2cf98-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cf98-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf98-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2cf98-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2cf98-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2cf98-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf98-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf98-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf98-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cf98-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf98-136">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="2cf98-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="2cf98-137">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="2cf98-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="2cf98-138">NLS: пример API-интерфейсов на основе имен</span><span class="sxs-lookup"><span data-stu-id="2cf98-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
