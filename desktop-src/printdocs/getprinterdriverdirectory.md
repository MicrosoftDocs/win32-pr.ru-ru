---
description: Функция Жетпринтердривердиректори извлекает путь к каталогу драйвера принтера.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Функция Жетпринтердривердиректори (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703136"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="bdf9a-103">Функция Жетпринтердривердиректори</span><span class="sxs-lookup"><span data-stu-id="bdf9a-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="bdf9a-104">Функция **жетпринтердривердиректори** извлекает путь к каталогу драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdf9a-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="bdf9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdf9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf9a-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором размещается драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="bdf9a-109">Если этот параметр имеет **значение NULL**, извлекается путь к каталогу локального драйвера.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9a-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-111">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="bdf9a-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="bdf9a-112">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="bdf9a-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9a-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-114">Уровень структуры.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-114">The structure level.</span></span> <span data-ttu-id="bdf9a-115">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9a-116">*пдривердиректори* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-117">Указатель на буфер, который получает путь.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9a-118">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-119">Размер буфера, на который указывает *пдривердиректори* .</span><span class="sxs-lookup"><span data-stu-id="bdf9a-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9a-120">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf9a-121">Указатель на значение, указывающее число байтов, скопированных при выполнении функции, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf9a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdf9a-122">Return value</span></span>

<span data-ttu-id="bdf9a-123">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bdf9a-124">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf9a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdf9a-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdf9a-126">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bdf9a-127">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bdf9a-128">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="bdf9a-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdf9a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bdf9a-129">Requirements</span></span>



| <span data-ttu-id="bdf9a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="bdf9a-130">Requirement</span></span> | <span data-ttu-id="bdf9a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf9a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf9a-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdf9a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf9a-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bdf9a-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdf9a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf9a-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bdf9a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bdf9a-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bdf9a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf9a-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdf9a-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bdf9a-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bdf9a-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdf9a-139"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdf9a-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bdf9a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bdf9a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdf9a-141"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bdf9a-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bdf9a-142">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="bdf9a-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bdf9a-143">**Жетпринтердривердиректорив** (Юникод) и **жетпринтердривердиректоря** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bdf9a-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bdf9a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdf9a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf9a-145">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="bdf9a-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bdf9a-146">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="bdf9a-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bdf9a-147">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="bdf9a-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




