---
description: Функция Жетпринтпроцессордиректори извлекает путь к каталогу обработчика печати на указанном сервере.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Функция Жетпринтпроцессордиректори (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913155"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="5bd6b-103">Функция Жетпринтпроцессордиректори</span><span class="sxs-lookup"><span data-stu-id="5bd6b-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="5bd6b-104">Функция **жетпринтпроцессордиректори** извлекает путь к каталогу обработчика печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bd6b-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="5bd6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bd6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd6b-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="5bd6b-109">Если этот параметр имеет **значение NULL**, то возвращается локальный путь.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6b-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-111">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="5bd6b-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="5bd6b-112">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="5bd6b-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6b-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-114">Уровень структуры.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-114">The structure level.</span></span> <span data-ttu-id="5bd6b-115">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6b-116">*ппринтпроцессоринфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-117">Указатель на буфер, который получает путь.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="5bd6b-118">Обратите внимание, что для операционных систем, предшествовавших Windows Server 2003 SP 1, путь имеет локальный формат сервера, а не истинный удаленный формат.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="5bd6b-119">Например, путь присваивается как "% WINDIR% \\ system32 \\ spool \\ пртпрокс \\ % окружения%" вместо " \\ \\ ServerName \\ Print $ \\ пртпрокс \\ % окружения%", даже при вызове для удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="5bd6b-120">Для операционных систем Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий возвращается истинный удаленный путь.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6b-121">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-122">Размер буфера, на который указывает *ппринтпроцессоринфо*.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6b-123">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6b-124">Указатель на значение, указывающее число байтов, скопированных при выполнении функции, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd6b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5bd6b-125">Return value</span></span>

<span data-ttu-id="5bd6b-126">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5bd6b-127">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd6b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bd6b-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5bd6b-129">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5bd6b-130">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5bd6b-131">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="5bd6b-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5bd6b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5bd6b-132">Requirements</span></span>



| <span data-ttu-id="5bd6b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5bd6b-133">Requirement</span></span> | <span data-ttu-id="5bd6b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5bd6b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd6b-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5bd6b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd6b-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5bd6b-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5bd6b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd6b-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5bd6b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5bd6b-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5bd6b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd6b-140"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd6b-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5bd6b-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5bd6b-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5bd6b-142"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bd6b-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5bd6b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd6b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd6b-144"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5bd6b-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5bd6b-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5bd6b-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5bd6b-146">**Жетпринтпроцессордиректорив** (Юникод) и **жетпринтпроцессордиректоря** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5bd6b-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5bd6b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bd6b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd6b-148">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5bd6b-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5bd6b-149">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="5bd6b-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5bd6b-150">**аддпринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="5bd6b-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




