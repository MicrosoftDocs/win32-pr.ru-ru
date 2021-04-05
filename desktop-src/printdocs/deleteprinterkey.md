---
description: Функция Делетепринтеркэй удаляет указанный ключ и все его подразделы для указанного принтера.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Функция Делетепринтеркэй (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815353"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="c0d7c-103">Функция Делетепринтеркэй</span><span class="sxs-lookup"><span data-stu-id="c0d7c-103">DeletePrinterKey function</span></span>

<span data-ttu-id="c0d7c-104">Функция **делетепринтеркэй** удаляет указанный ключ и все его подразделы для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0d7c-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="c0d7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0d7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d7c-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0d7c-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0d7c-108">Описатель принтера, для которого функция удаляет ключ.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="c0d7c-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c0d7c-110">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0d7c-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0d7c-111">Указатель на строку, завершающуюся нулем, которая указывает удаляемый ключ.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="c0d7c-112">Используйте символ обратной косой черты ( \\ ) в качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="c0d7c-113">Если *пкэйнаме* является пустой строкой (""), **делетепринтеркэй** удаляет все ключи ниже ключа верхнего уровня для принтера.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="c0d7c-114">Если *пкэйнаме* имеет **значение NULL**, **делетепринтеркэй** возвращает ошибку \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0d7c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0d7c-115">Return value</span></span>

<span data-ttu-id="c0d7c-116">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c0d7c-117">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0d7c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0d7c-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0d7c-119">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c0d7c-120">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c0d7c-121">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0d7c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c0d7c-122">Requirements</span></span>



| <span data-ttu-id="c0d7c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c0d7c-123">Requirement</span></span> | <span data-ttu-id="c0d7c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d7c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d7c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0d7c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d7c-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0d7c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c0d7c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0d7c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d7c-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0d7c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c0d7c-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c0d7c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0d7c-130"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7c-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c0d7c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0d7c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0d7c-132"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7c-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c0d7c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d7c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0d7c-134"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7c-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c0d7c-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c0d7c-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0d7c-136">**Делетепринтеркэйв** (Юникод) и **делетепринтеркэйа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c0d7c-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="c0d7c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0d7c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d7c-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="c0d7c-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="c0d7c-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-140">**делетепринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-141">**енумпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-142">**енумпринтеркэй**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-143">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-144">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c0d7c-145">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="c0d7c-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




