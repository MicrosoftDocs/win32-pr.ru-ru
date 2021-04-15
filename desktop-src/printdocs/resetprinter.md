---
description: Функция Ресетпринтер указывает тип данных и значения режима устройства, которые будут использоваться для печати документов, отправляемых функцией Стартдокпринтер. Эти значения можно переопределить с помощью функции Сетжоб после начала печати документа.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Функция Ресетпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702259"
---
# <a name="resetprinter-function"></a><span data-ttu-id="4108e-104">Функция Ресетпринтер</span><span class="sxs-lookup"><span data-stu-id="4108e-104">ResetPrinter function</span></span>

<span data-ttu-id="4108e-105">Функция **ресетпринтер** указывает тип данных и значения режима устройства, которые будут использоваться для печати документов, отправляемых функцией [**стартдокпринтер**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="4108e-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="4108e-106">Эти значения можно переопределить с помощью функции [**сетжоб**](setjob.md) после начала печати документа.</span><span class="sxs-lookup"><span data-stu-id="4108e-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="4108e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4108e-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="4108e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4108e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4108e-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4108e-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4108e-110">Обработайте с принтером.</span><span class="sxs-lookup"><span data-stu-id="4108e-110">Handle to the printer.</span></span> <span data-ttu-id="4108e-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="4108e-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4108e-112">*пдефаулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4108e-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4108e-113">Указатель на структуру [**\_ по умолчанию принтера**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="4108e-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="4108e-114">Функция **ресетпринтер** игнорирует элемент **десиредакцесс** структуры [**\_ по умолчанию принтера**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="4108e-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="4108e-115">Присвойте этому элементу нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4108e-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4108e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4108e-116">Return value</span></span>

<span data-ttu-id="4108e-117">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="4108e-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4108e-118">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4108e-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4108e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4108e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4108e-120">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="4108e-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4108e-121">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="4108e-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4108e-122">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="4108e-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4108e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4108e-123">Requirements</span></span>



| <span data-ttu-id="4108e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4108e-124">Requirement</span></span> | <span data-ttu-id="4108e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4108e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4108e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4108e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4108e-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4108e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4108e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4108e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4108e-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4108e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4108e-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4108e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4108e-131"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4108e-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4108e-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4108e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="4108e-133"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4108e-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4108e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4108e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4108e-135"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4108e-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4108e-136">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4108e-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4108e-137">**Ресетпринтерв** (Юникод) и **ресетпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4108e-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="4108e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4108e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4108e-139">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="4108e-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4108e-140">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="4108e-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4108e-141">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="4108e-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4108e-142">**\_значения по умолчанию для принтера**</span><span class="sxs-lookup"><span data-stu-id="4108e-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="4108e-143">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="4108e-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="4108e-144">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="4108e-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




