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
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "106011184"
---
# <a name="printerproperties-function"></a><span data-ttu-id="7a344-103">Функция Принтерпропертиес</span><span class="sxs-lookup"><span data-stu-id="7a344-103">PrinterProperties function</span></span>

<span data-ttu-id="7a344-104">Функция **принтерпропертиес** отображает страницу свойств принтера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="7a344-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a344-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a344-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="7a344-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a344-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a344-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a344-108">Маркер родительского окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7a344-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="7a344-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a344-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a344-110">Маркер объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="7a344-110">A handle to a printer object.</span></span> <span data-ttu-id="7a344-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="7a344-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a344-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a344-112">Return value</span></span>

<span data-ttu-id="7a344-113">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="7a344-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7a344-114">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7a344-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a344-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="7a344-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7a344-116">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="7a344-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7a344-117">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="7a344-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7a344-118">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="7a344-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a344-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7a344-119">Requirements</span></span>



| <span data-ttu-id="7a344-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7a344-120">Requirement</span></span> | <span data-ttu-id="7a344-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7a344-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a344-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a344-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a344-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a344-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a344-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a344-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a344-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a344-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a344-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a344-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a344-127"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a344-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7a344-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a344-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a344-129"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a344-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7a344-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a344-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a344-131"><dt>винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7a344-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a344-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a344-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a344-133">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="7a344-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7a344-134">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="7a344-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7a344-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="7a344-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="7a344-136">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="7a344-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




