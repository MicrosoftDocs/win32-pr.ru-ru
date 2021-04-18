---
description: Функция ScheduleJob запрашивает, что диспетчер очереди печати запланирует печать указанного задания печати.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Функция ScheduleJob (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712391"
---
# <a name="schedulejob-function"></a><span data-ttu-id="68aed-103">Функция ScheduleJob</span><span class="sxs-lookup"><span data-stu-id="68aed-103">ScheduleJob function</span></span>

<span data-ttu-id="68aed-104">Функция **ScheduleJob** запрашивает, что диспетчер очереди печати запланирует печать указанного задания печати.</span><span class="sxs-lookup"><span data-stu-id="68aed-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="68aed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68aed-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="68aed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68aed-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68aed-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68aed-108">Маркер принтера для задания печати.</span><span class="sxs-lookup"><span data-stu-id="68aed-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="68aed-109">Это должен быть локальный принтер, настроенный в качестве принтера с буферизацией.</span><span class="sxs-lookup"><span data-stu-id="68aed-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="68aed-110">Если *хпринтер* является маркером подключения к удаленному принтеру или если принтер настроен для прямой печати, функция **ScheduleJob** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="68aed-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="68aed-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="68aed-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="68aed-112">*хпринтер* должен быть одним и тем же маркером принтера, указанным в вызове [**AddJob**](addjob.md) , который получил идентификатор задания печати *двжобид* .</span><span class="sxs-lookup"><span data-stu-id="68aed-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="68aed-113">*двжобид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68aed-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68aed-114">Запланированное задание печати.</span><span class="sxs-lookup"><span data-stu-id="68aed-114">The print job to be scheduled.</span></span> <span data-ttu-id="68aed-115">Этот идентификатор задания печати можно получить, вызвав функцию [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="68aed-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68aed-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68aed-116">Return value</span></span>

<span data-ttu-id="68aed-117">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="68aed-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="68aed-118">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="68aed-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="68aed-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68aed-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68aed-120">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="68aed-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="68aed-121">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="68aed-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="68aed-122">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="68aed-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="68aed-123">Необходимо успешно вызвать функцию [**AddJob**](addjob.md) перед вызовом функции **ScheduleJob** .</span><span class="sxs-lookup"><span data-stu-id="68aed-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="68aed-124">**AddJob** получает идентификатор задания печати, который передается в **ScheduleJob** как *двжобид*.</span><span class="sxs-lookup"><span data-stu-id="68aed-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="68aed-125">Оба вызова должны использовать одно и то же значение для *хпринтер*.</span><span class="sxs-lookup"><span data-stu-id="68aed-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="68aed-126">Функция **ScheduleJob** проверяет наличие допустимого файла очереди.</span><span class="sxs-lookup"><span data-stu-id="68aed-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="68aed-127">Если имеется недопустимый файл буферизации или если он пуст, **ScheduleJob** удаляет файл очереди печати и соответствующую запись задания печати в диспетчере очереди.</span><span class="sxs-lookup"><span data-stu-id="68aed-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="68aed-128">Требования</span><span class="sxs-lookup"><span data-stu-id="68aed-128">Requirements</span></span>



| <span data-ttu-id="68aed-129">Требование</span><span class="sxs-lookup"><span data-stu-id="68aed-129">Requirement</span></span> | <span data-ttu-id="68aed-130">Значение</span><span class="sxs-lookup"><span data-stu-id="68aed-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68aed-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68aed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="68aed-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aed-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="68aed-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68aed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="68aed-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aed-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="68aed-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="68aed-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="68aed-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68aed-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="68aed-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68aed-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="68aed-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68aed-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="68aed-139">DLL</span><span class="sxs-lookup"><span data-stu-id="68aed-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68aed-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68aed-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="68aed-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68aed-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68aed-142">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="68aed-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="68aed-143">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="68aed-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="68aed-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="68aed-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="68aed-145">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="68aed-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




