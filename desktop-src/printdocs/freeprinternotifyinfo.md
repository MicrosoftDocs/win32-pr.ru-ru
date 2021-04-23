---
description: Функция Фрипринтернотифинфо освобождает выделенный системой буфер, созданный функцией Финднекстпринтерчанженотификатион.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Функция Фрипринтернотифинфо (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702213"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="0e9e1-103">Функция Фрипринтернотифинфо</span><span class="sxs-lookup"><span data-stu-id="0e9e1-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="0e9e1-104">Функция **фрипринтернотифинфо** освобождает выделенный системой буфер, созданный функцией [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="0e9e1-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e9e1-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0e9e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e9e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9e1-107">*ппринтернотифинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e9e1-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9e1-108">Указатель на буфер [**\_ \_ сведений об уведомлении принтера**](printer-notify-info.md) , возвращенный из вызова функции [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="0e9e1-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="0e9e1-109">**Фрипринтернотифинфо** освобождает этот буфер.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9e1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e9e1-110">Return value</span></span>

<span data-ttu-id="0e9e1-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0e9e1-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9e1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e9e1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e9e1-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0e9e1-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0e9e1-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="0e9e1-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e9e1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0e9e1-117">Requirements</span></span>



| <span data-ttu-id="0e9e1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0e9e1-118">Requirement</span></span> | <span data-ttu-id="0e9e1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0e9e1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9e1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e9e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9e1-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e9e1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e9e1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e9e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9e1-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e9e1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e9e1-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0e9e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9e1-125"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e1-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e9e1-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e9e1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e9e1-127"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e1-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0e9e1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0e9e1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9e1-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e1-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0e9e1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e9e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9e1-131">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="0e9e1-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0e9e1-132">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="0e9e1-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0e9e1-133">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="0e9e1-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="0e9e1-134">**\_сведения об уведомлении принтера \_**</span><span class="sxs-lookup"><span data-stu-id="0e9e1-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




