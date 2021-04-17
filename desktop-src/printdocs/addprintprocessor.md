---
description: Функция Аддпринтпроцессор устанавливает обработчик заданий печати на указанном сервере и добавляет имя обработчика печати в список поддерживаемых обработчиков печати.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Функция Аддпринтпроцессор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674229"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="b583f-103">Функция Аддпринтпроцессор</span><span class="sxs-lookup"><span data-stu-id="b583f-103">AddPrintProcessor function</span></span>

<span data-ttu-id="b583f-104">Функция **аддпринтпроцессор** устанавливает обработчик заданий печати на указанном сервере и добавляет имя обработчика печати в список поддерживаемых обработчиков печати.</span><span class="sxs-lookup"><span data-stu-id="b583f-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b583f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b583f-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="b583f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b583f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b583f-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b583f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b583f-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен обработчик печати.</span><span class="sxs-lookup"><span data-stu-id="b583f-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="b583f-109">Если этот параметр имеет **значение NULL**, обработчик заданий печати устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="b583f-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="b583f-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b583f-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b583f-111">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="b583f-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="b583f-112">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего или клиентского объекта (не целевого или сервера).</span><span class="sxs-lookup"><span data-stu-id="b583f-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="b583f-113">*ппаснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b583f-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b583f-114">Указатель на строку, завершающуюся нулем, которая указывает имя файла, содержащего обработчик заданий печати.</span><span class="sxs-lookup"><span data-stu-id="b583f-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="b583f-115">Этот файл должен находиться в каталоге системного процессора печати.</span><span class="sxs-lookup"><span data-stu-id="b583f-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="b583f-116">*ппринтпроцессорнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b583f-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b583f-117">Указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати.</span><span class="sxs-lookup"><span data-stu-id="b583f-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b583f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b583f-118">Return value</span></span>

<span data-ttu-id="b583f-119">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="b583f-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b583f-120">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b583f-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b583f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b583f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b583f-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="b583f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b583f-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="b583f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b583f-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="b583f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b583f-125">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="b583f-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="b583f-126">Перед вызовом функции **аддпринтпроцессор** приложение должно убедиться, что файл, содержащий обработчик заданий, хранится в системном каталоге системного принтера.</span><span class="sxs-lookup"><span data-stu-id="b583f-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="b583f-127">Приложение может получить имя каталога системного процессора, вызвав функцию [**жетпринтпроцессордиректори**](getprintprocessordirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="b583f-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="b583f-128">Приложение может определить имена существующих обработчиков печати, вызвав функцию [**енумпринтпроцессорс**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="b583f-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b583f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b583f-129">Requirements</span></span>



| <span data-ttu-id="b583f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b583f-130">Requirement</span></span> | <span data-ttu-id="b583f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b583f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b583f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b583f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b583f-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b583f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b583f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b583f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b583f-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b583f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b583f-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b583f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b583f-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b583f-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b583f-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b583f-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b583f-139"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b583f-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b583f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b583f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b583f-141"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b583f-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b583f-142">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b583f-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b583f-143">**Аддпринтпроцессорв** (Юникод) и **аддпринтпроцессора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b583f-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="b583f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b583f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b583f-145">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="b583f-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b583f-146">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="b583f-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b583f-147">**енумпринтпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="b583f-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="b583f-148">**жетпринтпроцессордиректори**</span><span class="sxs-lookup"><span data-stu-id="b583f-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

