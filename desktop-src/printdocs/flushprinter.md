---
description: Функция Флушпринтер отправляет буфер на принтер, чтобы очистить его из переходного состояния.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Функция Флушпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545354"
---
# <a name="flushprinter-function"></a><span data-ttu-id="62ae2-103">Функция Флушпринтер</span><span class="sxs-lookup"><span data-stu-id="62ae2-103">FlushPrinter function</span></span>

<span data-ttu-id="62ae2-104">Функция **флушпринтер** отправляет буфер на принтер, чтобы очистить его из переходного состояния.</span><span class="sxs-lookup"><span data-stu-id="62ae2-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ae2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62ae2-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="62ae2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ae2-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ae2-108">Маркер объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="62ae2-108">A handle to the printer object.</span></span> <span data-ttu-id="62ae2-109">Это должен быть тот же маркер, который использовался в предыдущем вызове [**вритепринтер**](writeprinter.md) драйвером принтера.</span><span class="sxs-lookup"><span data-stu-id="62ae2-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="62ae2-110">*пбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ae2-111">Указатель на массив байтов, содержащий данные, записываемые на принтер.</span><span class="sxs-lookup"><span data-stu-id="62ae2-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="62ae2-112">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ae2-113">Размер массива в байтах, на который указывает *пбуф*.</span><span class="sxs-lookup"><span data-stu-id="62ae2-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="62ae2-114">*пквриттен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ae2-115">Указатель на значение, которое получает число байтов данных, записанных на принтер.</span><span class="sxs-lookup"><span data-stu-id="62ae2-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="62ae2-116">*кслип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ae2-117">Время в миллисекундах, в течение которого строка ввода-вывода для порта принтера должна оставаться неактивной.</span><span class="sxs-lookup"><span data-stu-id="62ae2-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ae2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62ae2-118">Return value</span></span>

<span data-ttu-id="62ae2-119">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="62ae2-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="62ae2-120">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="62ae2-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="62ae2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62ae2-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62ae2-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="62ae2-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="62ae2-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="62ae2-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="62ae2-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="62ae2-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="62ae2-125">**Флушпринтер** должен вызываться только в случае сбоя [**вритепринтер**](writeprinter.md) , что приводит к переходу принтера в неизменное состояние.</span><span class="sxs-lookup"><span data-stu-id="62ae2-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="62ae2-126">Например, принтер может перейти в переходное состояние, когда задание прерывается и драйвер принтера частично отправил некоторые необработанные данные на принтер.</span><span class="sxs-lookup"><span data-stu-id="62ae2-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="62ae2-127">**Флушпринтер** также может указать период простоя, в течение которого диспетчер очереди печати не планирует задания на соответствующий порт принтера.</span><span class="sxs-lookup"><span data-stu-id="62ae2-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ae2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="62ae2-128">Requirements</span></span>



| <span data-ttu-id="62ae2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="62ae2-129">Requirement</span></span> | <span data-ttu-id="62ae2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="62ae2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ae2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62ae2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="62ae2-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="62ae2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62ae2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="62ae2-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62ae2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="62ae2-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="62ae2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ae2-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62ae2-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="62ae2-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62ae2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="62ae2-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62ae2-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="62ae2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="62ae2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ae2-140"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="62ae2-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="62ae2-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62ae2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ae2-142">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="62ae2-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="62ae2-143">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="62ae2-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="62ae2-144">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="62ae2-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




