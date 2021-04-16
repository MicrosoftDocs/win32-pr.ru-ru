---
description: Функция Жетдефаултпринтер извлекает имя принтера принтера по умолчанию для текущего пользователя на локальном компьютере.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Функция Жетдефаултпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693061"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="e5e70-103">Функция Жетдефаултпринтер</span><span class="sxs-lookup"><span data-stu-id="e5e70-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="e5e70-104">Функция **жетдефаултпринтер** извлекает имя принтера принтера по умолчанию для текущего пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e5e70-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5e70-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e5e70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5e70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e70-107">*псзбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5e70-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e70-108">Указатель на буфер, который получает строку символов, завершающуюся нулем, которая содержит имя принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5e70-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="e5e70-109">Если этот параметр имеет **значение NULL**, функция завершается ошибкой, и переменная, на которую указывает *пкчбуффер* , возвращает требуемый размер буфера в символах.</span><span class="sxs-lookup"><span data-stu-id="e5e70-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="e5e70-110">*пкчбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e5e70-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e70-111">В поле входные данные задает размер буфера *псзбуффер* в символах.</span><span class="sxs-lookup"><span data-stu-id="e5e70-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="e5e70-112">В выходных данных получает размер строки имени принтера в символах, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="e5e70-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e70-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e70-113">Return value</span></span>

<span data-ttu-id="e5e70-114">Если функция завершается удачно, возвращаемое значение является ненулевым значением, а переменная, на которую указывает *пкчбуффер* , содержит количество символов, скопированных в буфер *псзбуффер* , включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="e5e70-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="e5e70-115">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e5e70-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="e5e70-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e70-116">Value</span></span>                       | <span data-ttu-id="e5e70-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e70-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e70-118">Ошибка \_ недостаточного \_ буфера</span><span class="sxs-lookup"><span data-stu-id="e5e70-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="e5e70-119">Буфер *псзбуффер* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="e5e70-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="e5e70-120">Переменная, на которую указывает *пкчбуффер* , содержит требуемый размер буфера в символах.</span><span class="sxs-lookup"><span data-stu-id="e5e70-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="e5e70-121">\_файл ошибок \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="e5e70-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="e5e70-122">Принтер по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e5e70-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e5e70-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5e70-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5e70-124">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="e5e70-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e5e70-125">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="e5e70-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e5e70-126">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="e5e70-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5e70-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e5e70-127">Requirements</span></span>



| <span data-ttu-id="e5e70-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e5e70-128">Requirement</span></span> | <span data-ttu-id="e5e70-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e70-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e70-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5e70-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e70-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5e70-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5e70-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5e70-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e70-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5e70-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5e70-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5e70-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5e70-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5e70-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e5e70-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5e70-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5e70-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5e70-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e5e70-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e70-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e70-139"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e5e70-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e5e70-140">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e5e70-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e5e70-141">**Жетдефаултпринтерв** (Юникод) и **жетдефаултпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e5e70-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e5e70-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e70-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e70-143">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e5e70-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e5e70-144">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="e5e70-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e5e70-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="e5e70-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




