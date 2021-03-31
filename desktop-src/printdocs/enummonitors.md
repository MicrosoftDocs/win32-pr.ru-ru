---
description: Функция Енуммониторс извлекает сведения о мониторах портов, установленных на указанном сервере.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Функция Енуммониторс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813560"
---
# <a name="enummonitors-function"></a><span data-ttu-id="ffd54-103">Функция Енуммониторс</span><span class="sxs-lookup"><span data-stu-id="ffd54-103">EnumMonitors function</span></span>

<span data-ttu-id="ffd54-104">Функция **енуммониторс** извлекает сведения о мониторах портов, установленных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="ffd54-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffd54-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="ffd54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffd54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd54-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором находятся мониторы.</span><span class="sxs-lookup"><span data-stu-id="ffd54-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="ffd54-109">Если этот параметр имеет **значение NULL**, то выполняется перечисление локальных мониторов.</span><span class="sxs-lookup"><span data-stu-id="ffd54-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="ffd54-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-111">Версия структуры, на которую указывает *пмониторс*.</span><span class="sxs-lookup"><span data-stu-id="ffd54-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="ffd54-112">Это значение может быть равно 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="ffd54-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ffd54-113">*пмониторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-114">Указатель на буфер, который получает массив структур.</span><span class="sxs-lookup"><span data-stu-id="ffd54-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="ffd54-115">Буфер должен быть достаточно большим, чтобы хранить строки, на которые ссылаются члены структуры.</span><span class="sxs-lookup"><span data-stu-id="ffd54-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="ffd54-116">Чтобы определить требуемый размер буфера, вызовите **енуммониторс** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="ffd54-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="ffd54-117">**Енуммониторс** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="ffd54-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="ffd54-118">Если *уровень* равен 1, буфер получает массив структур из [**\_ сведений об мониторе \_ 1**](monitor-info-1.md) , или *Если уровень равен* 2, то при [**мониторинге структуры \_ \_ 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd54-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="ffd54-119">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-120">Размер (в байтах) буфера, на который указывает *пмониторс*.</span><span class="sxs-lookup"><span data-stu-id="ffd54-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="ffd54-121">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-122">Указатель на переменную, которая получает число байтов, скопированных, если функция выполнена, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="ffd54-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="ffd54-123">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd54-124">Указатель на переменную, которая получает количество структур, возвращенных в буфере, на который указывает *пмониторс*.</span><span class="sxs-lookup"><span data-stu-id="ffd54-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd54-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffd54-125">Return value</span></span>

<span data-ttu-id="ffd54-126">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="ffd54-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ffd54-127">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ffd54-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd54-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffd54-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ffd54-129">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="ffd54-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ffd54-130">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="ffd54-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ffd54-131">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="ffd54-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ffd54-132">Требования</span><span class="sxs-lookup"><span data-stu-id="ffd54-132">Requirements</span></span>



| <span data-ttu-id="ffd54-133">Требование</span><span class="sxs-lookup"><span data-stu-id="ffd54-133">Requirement</span></span> | <span data-ttu-id="ffd54-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ffd54-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd54-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffd54-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd54-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ffd54-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffd54-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd54-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ffd54-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ffd54-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ffd54-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd54-140"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd54-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ffd54-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ffd54-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffd54-142"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffd54-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ffd54-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ffd54-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd54-144"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ffd54-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ffd54-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ffd54-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ffd54-146">**Енуммониторсв** (Юникод) и **енуммониторса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ffd54-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="ffd54-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffd54-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd54-148">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ffd54-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ffd54-149">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="ffd54-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ffd54-150">**\_Сведения о мониторе \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ffd54-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="ffd54-151">**\_Сведения о мониторе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ffd54-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

