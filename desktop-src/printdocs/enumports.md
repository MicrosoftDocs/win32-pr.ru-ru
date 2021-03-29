---
description: Функция Енумпортс перечисляет порты, доступные для печати на указанном сервере.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Функция Енумпортс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647489"
---
# <a name="enumports-function"></a><span data-ttu-id="11853-103">Функция Енумпортс</span><span class="sxs-lookup"><span data-stu-id="11853-103">EnumPorts function</span></span>

<span data-ttu-id="11853-104">Функция **енумпортс** перечисляет порты, доступные для печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="11853-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="11853-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11853-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="11853-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11853-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11853-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, порты принтера которого требуется перечислить.</span><span class="sxs-lookup"><span data-stu-id="11853-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="11853-109">Если *pName* имеет **значение NULL**, функция перечисляет порты принтера на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="11853-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="11853-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11853-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-111">Тип сведений, возвращаемых в буфер *ппортс* .</span><span class="sxs-lookup"><span data-stu-id="11853-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="11853-112">Если *уровень* равен 1, *ппортс* получает массив структур [**\_ info \_ 1**](port-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="11853-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="11853-113">Если *уровень* равен 2, *ппортс* получает массив структур [**\_ info \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="11853-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="11853-114">*ппортс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11853-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-115">Указатель на буфер, который получает массив из структур сведений о [**порте \_ \_ 1**](port-info-1.md) или [**порт \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="11853-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="11853-116">Каждая структура содержит данные, описывающие доступный порт принтера.</span><span class="sxs-lookup"><span data-stu-id="11853-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="11853-117">Буфер должен быть достаточно большим, чтобы хранить строки, на которые указывает члены структуры.</span><span class="sxs-lookup"><span data-stu-id="11853-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="11853-118">Чтобы определить требуемый размер буфера, вызовите **енумпортс** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="11853-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="11853-119">**Енумпортс** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="11853-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="11853-120">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11853-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-121">Размер (в байтах) буфера, на который указывает *ппортс*.</span><span class="sxs-lookup"><span data-stu-id="11853-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="11853-122">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11853-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-123">Указатель на переменную, которая получает число байтов, скопированных в буфер *ппортс* .</span><span class="sxs-lookup"><span data-stu-id="11853-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="11853-124">Если буфер слишком мал, функция завершается ошибкой и переменная получает необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="11853-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="11853-125">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11853-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11853-126">Указатель на переменную, которая получает количество структур сведений о [**портах \_ \_ 1**](port-info-1.md) или Port, возвращенных в буфере *ппортс* . [**\_ \_**](port-info-2.md)</span><span class="sxs-lookup"><span data-stu-id="11853-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="11853-127">Число портов принтера, доступных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="11853-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11853-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11853-128">Return value</span></span>

<span data-ttu-id="11853-129">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="11853-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="11853-130">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="11853-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="11853-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11853-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11853-132">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="11853-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="11853-133">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="11853-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="11853-134">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="11853-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="11853-135">Функция **енумпортс** может быть выполнена успешно, даже если на сервере, указанном в *pName* , не определен принтер.</span><span class="sxs-lookup"><span data-stu-id="11853-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="11853-136">Требования</span><span class="sxs-lookup"><span data-stu-id="11853-136">Requirements</span></span>



| <span data-ttu-id="11853-137">Требование</span><span class="sxs-lookup"><span data-stu-id="11853-137">Requirement</span></span> | <span data-ttu-id="11853-138">Значение</span><span class="sxs-lookup"><span data-stu-id="11853-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11853-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11853-139">Minimum supported client</span></span><br/> | <span data-ttu-id="11853-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11853-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11853-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11853-141">Minimum supported server</span></span><br/> | <span data-ttu-id="11853-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11853-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11853-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11853-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="11853-144"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11853-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="11853-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11853-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="11853-146"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11853-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="11853-147">DLL</span><span class="sxs-lookup"><span data-stu-id="11853-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11853-148"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="11853-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="11853-149">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="11853-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11853-150">**Енумпортсв** (Юникод) и **енумпортса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11853-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="11853-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11853-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11853-152">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="11853-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="11853-153">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="11853-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="11853-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="11853-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="11853-155">**делетепорт**</span><span class="sxs-lookup"><span data-stu-id="11853-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="11853-156">**\_Сведения о порте \_ 1**</span><span class="sxs-lookup"><span data-stu-id="11853-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="11853-157">**\_Сведения о порте \_ 2**</span><span class="sxs-lookup"><span data-stu-id="11853-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

