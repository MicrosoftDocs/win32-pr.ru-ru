---
description: Функция Финдклосепринтерчанженотификатион закрывает объект уведомления об изменении, созданный путем вызова функции Финдфирстпринтерчанженотификатион.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Функция Финдклосепринтерчанженотификатион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080742"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="34d55-103">Функция Финдклосепринтерчанженотификатион</span><span class="sxs-lookup"><span data-stu-id="34d55-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="34d55-104">Функция **финдклосепринтерчанженотификатион** закрывает объект уведомления об изменении, созданный путем вызова функции [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="34d55-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="34d55-105">Этот объект больше не будет отслеживать принтер или сервер печати, связанный с объектом уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="34d55-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34d55-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="34d55-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34d55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34d55-108">*хчанже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34d55-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d55-109">Описатель для закрытого объекта уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="34d55-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="34d55-110">Это маркер, созданный путем вызова функции [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="34d55-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34d55-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34d55-111">Return value</span></span>

<span data-ttu-id="34d55-112">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="34d55-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="34d55-113">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="34d55-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d55-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34d55-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34d55-115">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="34d55-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="34d55-116">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="34d55-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="34d55-117">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="34d55-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="34d55-118">После вызова функции **финдклосепринтерчанженотификатион** нельзя использовать маркер *хчанже* в последующих вызовах [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) или [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="34d55-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34d55-119">Требования</span><span class="sxs-lookup"><span data-stu-id="34d55-119">Requirements</span></span>



| <span data-ttu-id="34d55-120">Требование</span><span class="sxs-lookup"><span data-stu-id="34d55-120">Requirement</span></span> | <span data-ttu-id="34d55-121">Значение</span><span class="sxs-lookup"><span data-stu-id="34d55-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34d55-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34d55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="34d55-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34d55-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="34d55-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34d55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="34d55-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34d55-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="34d55-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="34d55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="34d55-127"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34d55-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="34d55-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34d55-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="34d55-129"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34d55-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="34d55-130">DLL</span><span class="sxs-lookup"><span data-stu-id="34d55-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34d55-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34d55-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="34d55-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34d55-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d55-133">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="34d55-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="34d55-134">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="34d55-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="34d55-135">**финдфирстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="34d55-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="34d55-136">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="34d55-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




