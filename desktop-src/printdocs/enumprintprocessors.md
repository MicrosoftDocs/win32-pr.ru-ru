---
description: Функция Енумпринтпроцессорс перечисляет обработчики печати, установленные на указанном сервере.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Функция Енумпринтпроцессорс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998849"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="8ff3c-103">Функция Енумпринтпроцессорс</span><span class="sxs-lookup"><span data-stu-id="8ff3c-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="8ff3c-104">Функция **енумпринтпроцессорс** перечисляет обработчики печати, установленные на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ff3c-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="8ff3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ff3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff3c-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором находятся обработчики печати.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="8ff3c-109">Если этот параметр имеет **значение NULL**, локальные обработчики печати перечисляются.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-111">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="8ff3c-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="8ff3c-112">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="8ff3c-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-114">Тип сведений, возвращаемых в буфер *ппринтпроцессоринфо* .</span><span class="sxs-lookup"><span data-stu-id="8ff3c-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="8ff3c-115">Этот параметр должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-116">*ппринтпроцессоринфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-117">Указатель на буфер, который получает массив структур [**принтпроцессор \_ info \_ 1**](printprocessor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="8ff3c-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="8ff3c-118">Каждая структура описывает доступный обработчик печати.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="8ff3c-119">Буфер должен быть достаточно большим, чтобы получить массив структур и все строки, на которые указывает элемент структуры.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="8ff3c-120">Чтобы определить требуемый размер буфера, вызовите **енумпринтпроцессорс** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="8ff3c-121">**Енумпринтпроцессорс** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-122">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-123">Размер (в байтах) буфера, на который указывает *ппринтпроцессоринфо*.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-124">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-125">Указатель на переменную, которая получает число байтов, скопированных в буфер *ппринтпроцессоринфо* , если функция выполнена.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="8ff3c-126">Если буфер слишком мал, функция завершается ошибкой и переменная получает необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="8ff3c-127">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff3c-128">Указатель на переменную, которая получает количество структур, возвращенных в буфере *ппринтпроцессоринфо* .</span><span class="sxs-lookup"><span data-stu-id="8ff3c-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff3c-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ff3c-129">Return value</span></span>

<span data-ttu-id="8ff3c-130">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8ff3c-131">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff3c-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ff3c-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ff3c-133">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8ff3c-134">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8ff3c-135">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8ff3c-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ff3c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="8ff3c-136">Requirements</span></span>



| <span data-ttu-id="8ff3c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="8ff3c-137">Requirement</span></span> | <span data-ttu-id="8ff3c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="8ff3c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff3c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ff3c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff3c-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ff3c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ff3c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff3c-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ff3c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ff3c-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ff3c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff3c-144"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff3c-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8ff3c-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ff3c-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ff3c-146"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ff3c-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8ff3c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff3c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff3c-148"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8ff3c-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8ff3c-149">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8ff3c-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8ff3c-150">**Енумпринтпроцессорсв** (Юникод) и **енумпринтпроцессорса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8ff3c-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="8ff3c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ff3c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff3c-152">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8ff3c-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8ff3c-153">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8ff3c-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8ff3c-154">**аддпринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="8ff3c-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="8ff3c-155">**енумпринтпроцессордататипес**</span><span class="sxs-lookup"><span data-stu-id="8ff3c-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="8ff3c-156">**\_Сведения о принтпроцессор \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8ff3c-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

