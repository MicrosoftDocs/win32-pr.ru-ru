---
description: Функция Енумпринтпроцессордататипес перечисляет типы данных, поддерживаемые указанным обработчиком печати.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Функция Енумпринтпроцессордататипес (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545359"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="8dfc0-103">Функция Енумпринтпроцессордататипес</span><span class="sxs-lookup"><span data-stu-id="8dfc0-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="8dfc0-104">Функция **енумпринтпроцессордататипес** перечисляет типы данных, поддерживаемые указанным обработчиком печати.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dfc0-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="8dfc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8dfc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dfc0-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором находится обработчик печати.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="8dfc0-109">Если этот параметр имеет **значение NULL**, то перечисляются типы данных для локального обработчика печати.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-110">*ппринтпроцессорнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-111">Указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати, для которого перечисляются типы данных.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-112">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-113">Тип сведений, возвращаемых в буфер *пдататипес* .</span><span class="sxs-lookup"><span data-stu-id="8dfc0-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="8dfc0-114">Этот параметр должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-115">*пдататипес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-116">Указатель на буфер, который получает массив данных с данными [**\_ \_ 1**](datatypes-info-1.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="8dfc0-117">Каждая структура описывает доступный тип данных.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-117">Each structure describes an available data type.</span></span> <span data-ttu-id="8dfc0-118">Буфер должен быть достаточно большим, чтобы получать массив структур и любые строки или другие данные, к которым она указывает.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="8dfc0-119">Чтобы определить требуемый размер буфера, вызовите **енумпринтпроцессордататипес** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="8dfc0-120">**Енумпринтпроцессордататипес** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-121">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-122">Размер (в байтах) буфера, на который указывает *пдататипес*.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-123">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-124">Указатель на переменную, которая получает число байтов, скопированных в буфер *пдататипес* , если функция выполнена.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="8dfc0-125">Если буфер слишком мал, функция завершается ошибкой и переменная получает необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-126">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfc0-127">Указатель на переменную, которая получает количество структур, возвращенных в буфере *пдататипес* .</span><span class="sxs-lookup"><span data-stu-id="8dfc0-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="8dfc0-128">Число поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dfc0-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dfc0-129">Return value</span></span>

<span data-ttu-id="8dfc0-130">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8dfc0-131">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfc0-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8dfc0-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8dfc0-133">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8dfc0-134">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8dfc0-135">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8dfc0-136">v</span><span class="sxs-lookup"><span data-stu-id="8dfc0-136">v</span></span>

<span data-ttu-id="8dfc0-137">Начиная с Windows Vista, сведения о типах данных с удаленных серверов печати извлекаются из локального кэша.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfc0-138">Требования</span><span class="sxs-lookup"><span data-stu-id="8dfc0-138">Requirements</span></span>



| <span data-ttu-id="8dfc0-139">Требование</span><span class="sxs-lookup"><span data-stu-id="8dfc0-139">Requirement</span></span> | <span data-ttu-id="8dfc0-140">Значение</span><span class="sxs-lookup"><span data-stu-id="8dfc0-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfc0-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dfc0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfc0-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8dfc0-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dfc0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfc0-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8dfc0-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8dfc0-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8dfc0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dfc0-146"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8dfc0-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8dfc0-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8dfc0-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="8dfc0-148"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dfc0-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8dfc0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8dfc0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dfc0-150"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8dfc0-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8dfc0-151">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8dfc0-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8dfc0-152">**Енумпринтпроцессордататипесв** (Юникод) и **енумпринтпроцессордататипеса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8dfc0-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8dfc0-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dfc0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfc0-154">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8dfc0-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8dfc0-155">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8dfc0-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8dfc0-156">**\_Сведения о типах данных \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="8dfc0-157">**енумпринтпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

