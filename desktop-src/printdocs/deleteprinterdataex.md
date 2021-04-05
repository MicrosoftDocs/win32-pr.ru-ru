---
description: Функция Делетепринтердатаекс удаляет указанное значение из данных конфигурации для принтера.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Функция Делетепринтердатаекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814873"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="bf116-103">Функция Делетепринтердатаекс</span><span class="sxs-lookup"><span data-stu-id="bf116-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="bf116-104">Функция **делетепринтердатаекс** удаляет указанное значение из данных конфигурации для принтера.</span><span class="sxs-lookup"><span data-stu-id="bf116-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="bf116-105">Данные конфигурации принтера состоят из набора именованных и типизированных значений, хранящихся в иерархии разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="bf116-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="bf116-106">Функция удаляет указанное значение в указанном ключе.</span><span class="sxs-lookup"><span data-stu-id="bf116-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="bf116-107">Как и функция [**делетепринтердата**](deleteprinterdata.md) , **делетепринтердатаекс** может удалять значения, хранящиеся в функции [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bf116-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="bf116-108">Кроме того, **делетепринтердатаекс** может удалять значения, хранящиеся в указанном ключе функцией [**сетпринтердатаекс**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="bf116-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf116-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf116-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="bf116-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf116-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf116-111">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf116-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf116-112">Описатель принтера, для которого функция удаляет значение.</span><span class="sxs-lookup"><span data-stu-id="bf116-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="bf116-113">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="bf116-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bf116-114">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf116-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf116-115">Указатель на строку, завершающуюся нулем, которая указывает ключ, содержащий удаляемое значение.</span><span class="sxs-lookup"><span data-stu-id="bf116-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="bf116-116">Используйте символ обратной косой черты ( \\ ) в качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="bf116-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="bf116-117">Если *пкэйнаме* имеет **значение NULL** или является пустой строкой, **делетепринтердатаекс** возвращает ошибку \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="bf116-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="bf116-118">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf116-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf116-119">Указатель на строку, завершающуюся нулем, которая указывает имя удаляемого значения.</span><span class="sxs-lookup"><span data-stu-id="bf116-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf116-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf116-120">Return value</span></span>

<span data-ttu-id="bf116-121">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf116-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bf116-122">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="bf116-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf116-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf116-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf116-124">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="bf116-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bf116-125">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="bf116-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bf116-126">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="bf116-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf116-127">Требования</span><span class="sxs-lookup"><span data-stu-id="bf116-127">Requirements</span></span>



| <span data-ttu-id="bf116-128">Требование</span><span class="sxs-lookup"><span data-stu-id="bf116-128">Requirement</span></span> | <span data-ttu-id="bf116-129">Значение</span><span class="sxs-lookup"><span data-stu-id="bf116-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf116-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf116-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bf116-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf116-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bf116-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf116-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bf116-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf116-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf116-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bf116-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf116-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf116-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bf116-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf116-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf116-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf116-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bf116-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bf116-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf116-139"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bf116-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bf116-140">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="bf116-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf116-141">**Делетепринтердатаексв** (Юникод) и **делетепринтердатаекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf116-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bf116-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf116-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf116-143">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="bf116-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bf116-144">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="bf116-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bf116-145">**делетепринтеркэй**</span><span class="sxs-lookup"><span data-stu-id="bf116-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="bf116-146">**енумпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="bf116-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="bf116-147">**енумпринтеркэй**</span><span class="sxs-lookup"><span data-stu-id="bf116-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="bf116-148">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="bf116-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="bf116-149">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="bf116-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bf116-150">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="bf116-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




