---
description: Функция SetDefaultPrinter задает имя принтера принтера по умолчанию для текущего пользователя на локальном компьютере.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Функция SetDefaultPrinter (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712388"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="f0a1c-103">Функция SetDefaultPrinter</span><span class="sxs-lookup"><span data-stu-id="f0a1c-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="f0a1c-104">Функция **SetDefaultPrinter** задает имя принтера принтера по умолчанию для текущего пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0a1c-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="f0a1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a1c-107">*псзпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0a1c-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a1c-108">Указатель на строку с завершающим нулем, содержащую имя принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="f0a1c-109">Для подключения к удаленному принтеру используется формат имени **\\\\** _сервера_ *_\\_* _принтернаме_.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="f0a1c-110">Для локального принтера используется формат имени *принтернаме*.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="f0a1c-111">Если этот параметр имеет **значение NULL** или является пустой строкой, то есть "", **SetDefaultPrinter** выберет принтер по умолчанию на одном из установленных принтеров.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="f0a1c-112">Если принтер по умолчанию уже существует, вызов **SetDefaultPrinter** с **нулевым значением** или пустой строкой в этом параметре может изменить принтер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a1c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0a1c-113">Return value</span></span>

<span data-ttu-id="f0a1c-114">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f0a1c-115">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a1c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0a1c-116">Remarks</span></span>

<span data-ttu-id="f0a1c-117">При использовании этого метода необходимо указать допустимый принтер, драйвер и порт.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="f0a1c-118">Если они недопустимы, то API-интерфейсы не завершаются ошибкой, но результат не определен.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="f0a1c-119">Это может привести к тому, что другие программы снова настроили принтер на предыдущий допустимый принтер.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="f0a1c-120">[**Енумпринтерс**](enumprinters.md) можно использовать для получения имени принтера, имени драйвера и имени порта всех доступных принтеров.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="f0a1c-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f0a1c-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f0a1c-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="f0a1c-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0a1c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f0a1c-124">Requirements</span></span>



| <span data-ttu-id="f0a1c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f0a1c-125">Requirement</span></span> | <span data-ttu-id="f0a1c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a1c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a1c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0a1c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a1c-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0a1c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f0a1c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0a1c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a1c-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0a1c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f0a1c-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f0a1c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a1c-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0a1c-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f0a1c-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f0a1c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0a1c-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0a1c-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f0a1c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a1c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a1c-136"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f0a1c-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f0a1c-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f0a1c-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0a1c-138">**Сетдефаултпринтерв** (Юникод) и **сетдефаултпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f0a1c-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="f0a1c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0a1c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a1c-140">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f0a1c-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f0a1c-141">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="f0a1c-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f0a1c-142">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="f0a1c-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="f0a1c-143">**жетдефаултпринтер**</span><span class="sxs-lookup"><span data-stu-id="f0a1c-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




