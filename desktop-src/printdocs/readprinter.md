---
description: Функция Реадпринтер извлекает данные с указанного принтера.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Функция Реадпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693237"
---
# <a name="readprinter-function"></a><span data-ttu-id="6105f-103">Функция Реадпринтер</span><span class="sxs-lookup"><span data-stu-id="6105f-103">ReadPrinter function</span></span>

<span data-ttu-id="6105f-104">Функция **реадпринтер** извлекает данные с указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="6105f-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6105f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6105f-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="6105f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6105f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6105f-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6105f-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6105f-108">Описатель объекта принтера, для которого необходимо получить данные.</span><span class="sxs-lookup"><span data-stu-id="6105f-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="6105f-109">Используйте функцию [**опенпринтер**](openprinter.md) для получения маркера объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="6105f-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="6105f-110">Используйте формат: Принтернаме, задание XXXX.</span><span class="sxs-lookup"><span data-stu-id="6105f-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="6105f-111">*пбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6105f-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6105f-112">Указатель на буфер, который получает данные принтера.</span><span class="sxs-lookup"><span data-stu-id="6105f-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="6105f-113">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6105f-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6105f-114">Размер (в байтах) буфера, на который *пбуф* указывает.</span><span class="sxs-lookup"><span data-stu-id="6105f-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="6105f-115">*пнобитесреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6105f-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6105f-116">Указатель на переменную, которая получает число байтов данных, копируемых в массив, в который *пбуф* Points.</span><span class="sxs-lookup"><span data-stu-id="6105f-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6105f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6105f-117">Return value</span></span>

<span data-ttu-id="6105f-118">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6105f-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6105f-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6105f-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6105f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6105f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6105f-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6105f-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6105f-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="6105f-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6105f-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="6105f-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6105f-124">**Реадпринтер** возвращает ошибку, если устройство или принтер не являются двунаправленными.</span><span class="sxs-lookup"><span data-stu-id="6105f-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6105f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6105f-125">Requirements</span></span>



| <span data-ttu-id="6105f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6105f-126">Requirement</span></span> | <span data-ttu-id="6105f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6105f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6105f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6105f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6105f-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6105f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6105f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6105f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6105f-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6105f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6105f-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6105f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6105f-133"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6105f-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6105f-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6105f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6105f-135"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6105f-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6105f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6105f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6105f-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6105f-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6105f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6105f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6105f-139">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6105f-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6105f-140">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6105f-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6105f-141">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="6105f-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




