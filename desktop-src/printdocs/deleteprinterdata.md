---
description: Функция Делетепринтердата удаляет указанные данные конфигурации для принтера. Данные конфигурации принтеров состоят из набора именованных и типизированных значений. Функция Делетепринтердата удаляет одно из этих значений, указанное по имени значения.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Функция Делетепринтердата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345312"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="ee9c4-105">Функция Делетепринтердата</span><span class="sxs-lookup"><span data-stu-id="ee9c4-105">DeletePrinterData function</span></span>

<span data-ttu-id="ee9c4-106">Функция **делетепринтердата** удаляет указанные данные конфигурации для принтера.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="ee9c4-107">Данные конфигурации принтера состоят из набора именованных и типизированных значений.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="ee9c4-108">Функция **делетепринтердата** удаляет одно из этих значений, указанное по имени значения.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="ee9c4-109">Вызов **делетепринтердата** эквивалентен вызову функции [**делетепринтердатаекс**](deleteprinterdataex.md) с параметром *Пкэйнаме* , имеющим значение "принтердривердата".</span><span class="sxs-lookup"><span data-stu-id="ee9c4-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9c4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee9c4-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="ee9c4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee9c4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee9c4-112">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee9c4-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9c4-113">Описатель принтера, данные конфигурации которого необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="ee9c4-114">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ee9c4-115">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee9c4-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9c4-116">Указатель на имя удаляемого значения данных конфигурации, заканчивающееся нулем.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee9c4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee9c4-117">Return value</span></span>

<span data-ttu-id="ee9c4-118">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ee9c4-119">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee9c4-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee9c4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee9c4-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ee9c4-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ee9c4-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee9c4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ee9c4-124">Requirements</span></span>



| <span data-ttu-id="ee9c4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ee9c4-125">Requirement</span></span> | <span data-ttu-id="ee9c4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ee9c4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9c4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee9c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9c4-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee9c4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee9c4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee9c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9c4-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee9c4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee9c4-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ee9c4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee9c4-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee9c4-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee9c4-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee9c4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee9c4-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee9c4-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ee9c4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ee9c4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee9c4-136"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ee9c4-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ee9c4-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ee9c4-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ee9c4-138">**Делетепринтердатав** (Юникод) и **делетепринтердатаа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ee9c4-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ee9c4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee9c4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9c4-140">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ee9c4-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-141">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="ee9c4-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-142">**енумпринтердата**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-143">**жетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-144">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-145">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="ee9c4-146">**сетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




