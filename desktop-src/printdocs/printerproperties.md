---
description: Функция Принтерпропертиес отображает страницу свойств принтера для указанного принтера.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Функция Принтерпропертиес (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
ms.openlocfilehash: ca6a238b73700219a3c79bd8d2369bf155633f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712156"
---
# <a name="printerproperties-function"></a><span data-ttu-id="ce43e-103">Функция Принтерпропертиес</span><span class="sxs-lookup"><span data-stu-id="ce43e-103">PrinterProperties function</span></span>

<span data-ttu-id="ce43e-104">Функция **принтерпропертиес** отображает страницу свойств принтера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="ce43e-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce43e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce43e-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="ce43e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce43e-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce43e-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce43e-108">Маркер родительского окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="ce43e-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="ce43e-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce43e-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce43e-110">Маркер объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="ce43e-110">A handle to a printer object.</span></span> <span data-ttu-id="ce43e-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="ce43e-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce43e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce43e-112">Return value</span></span>

<span data-ttu-id="ce43e-113">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="ce43e-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ce43e-114">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ce43e-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce43e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce43e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce43e-116">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="ce43e-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ce43e-117">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="ce43e-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ce43e-118">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="ce43e-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce43e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ce43e-119">Requirements</span></span>



| <span data-ttu-id="ce43e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ce43e-120">Requirement</span></span> | <span data-ttu-id="ce43e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ce43e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce43e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce43e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce43e-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce43e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce43e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce43e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce43e-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce43e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce43e-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ce43e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce43e-127"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce43e-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce43e-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce43e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce43e-129"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce43e-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ce43e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ce43e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce43e-131"><dt>Plotui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce43e-131"><dt>Plotui.dll</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ce43e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce43e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce43e-133">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ce43e-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce43e-134">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="ce43e-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ce43e-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="ce43e-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="ce43e-136">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="ce43e-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




