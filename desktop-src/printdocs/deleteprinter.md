---
description: Функция Делетепринтер удаляет указанный объект принтера.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Функция Делетепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693040"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="762cb-103">Функция Делетепринтер</span><span class="sxs-lookup"><span data-stu-id="762cb-103">DeletePrinter function</span></span>

<span data-ttu-id="762cb-104">Функция **делетепринтер** удаляет указанный объект принтера.</span><span class="sxs-lookup"><span data-stu-id="762cb-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="762cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="762cb-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="762cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="762cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762cb-107">*хпринтер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="762cb-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="762cb-108">Обрабатывает объект принтера, который будет удален.</span><span class="sxs-lookup"><span data-stu-id="762cb-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="762cb-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="762cb-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762cb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="762cb-110">Return value</span></span>

<span data-ttu-id="762cb-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="762cb-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="762cb-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="762cb-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="762cb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="762cb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="762cb-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="762cb-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="762cb-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="762cb-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="762cb-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="762cb-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="762cb-117">Если для указанного принтера имеются оставшиеся задания печати, **делетепринтер** помечает принтер на ожидание удаления, а затем удаляет его после печати всех заданий печати.</span><span class="sxs-lookup"><span data-stu-id="762cb-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="762cb-118">Не удается добавить задания печати на принтер, помеченный для ожидающего удаления.</span><span class="sxs-lookup"><span data-stu-id="762cb-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="762cb-119">Принтер, помеченный для ожидающего удаления, не может удерживаться, но его задания печати можно хранить, возобновлять и перезапускать.</span><span class="sxs-lookup"><span data-stu-id="762cb-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="762cb-120">Если принтер удерживается и имеются задания для принтера, **делетепринтер** завершается с ошибкой \_ отказа в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="762cb-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="762cb-121">Обратите внимание, что **делетепринтер** не закрывает переданный ему обработчик.</span><span class="sxs-lookup"><span data-stu-id="762cb-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="762cb-122">Поэтому приложение по-прежнему должно вызывать [**клосепринтер**](closeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="762cb-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="762cb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="762cb-123">Requirements</span></span>



| <span data-ttu-id="762cb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="762cb-124">Requirement</span></span> | <span data-ttu-id="762cb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="762cb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="762cb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="762cb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="762cb-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="762cb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="762cb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="762cb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="762cb-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="762cb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="762cb-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="762cb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="762cb-131"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="762cb-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="762cb-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="762cb-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="762cb-133"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="762cb-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="762cb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="762cb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="762cb-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="762cb-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="762cb-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="762cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762cb-137">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="762cb-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="762cb-138">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="762cb-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="762cb-139">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="762cb-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="762cb-140">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="762cb-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="762cb-141">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="762cb-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




