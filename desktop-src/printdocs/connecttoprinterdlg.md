---
description: Функция Коннекттопринтердлг отображает диалоговое окно, позволяющее пользователям просматривать принтеры в сети и подключаться к ним.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Функция Коннекттопринтердлг (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674281"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="e8fab-103">Функция Коннекттопринтердлг</span><span class="sxs-lookup"><span data-stu-id="e8fab-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="e8fab-104">Функция **коннекттопринтердлг** отображает диалоговое окно, позволяющее пользователям просматривать принтеры в сети и подключаться к ним.</span><span class="sxs-lookup"><span data-stu-id="e8fab-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="e8fab-105">Если пользователь выбирает принтер, функция пытается создать соединение с ним; Если подходящий драйвер не установлен на сервере, пользователю предоставляется возможность создать принтер локально.</span><span class="sxs-lookup"><span data-stu-id="e8fab-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8fab-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e8fab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8fab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fab-108">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8fab-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fab-109">Указывает родительское окно диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="e8fab-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e8fab-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8fab-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fab-111">Этот параметр зарезервирован и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e8fab-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fab-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8fab-112">Return value</span></span>

<span data-ttu-id="e8fab-113">Если функция выполнена удачно и пользователь выбирает принтер, возвращаемое значение является маркером выбранного принтера.</span><span class="sxs-lookup"><span data-stu-id="e8fab-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="e8fab-114">Если функция завершается ошибкой или пользователь отменяет диалоговое окно, не выбирая принтер, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e8fab-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fab-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8fab-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8fab-116">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="e8fab-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e8fab-117">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="e8fab-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e8fab-118">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="e8fab-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e8fab-119">Функция **коннекттопринтердлг** пытается создать подключение к выбранному принтеру.</span><span class="sxs-lookup"><span data-stu-id="e8fab-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="e8fab-120">Однако если на сервере, на котором находится принтер, не установлен подходящий драйвер, функция предлагает пользователю возможность создания принтера локально.</span><span class="sxs-lookup"><span data-stu-id="e8fab-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="e8fab-121">Вызывающее приложение может определить, был ли функция создала принтер локально, вызвав метод «The [**PrintOut**](getprinter.md) » со структурой « [**Printer \_ info \_ 2**](printer-info-2.md) », а затем изучен элемент **атрибутов** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="e8fab-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="e8fab-122">Приложение должно вызывать [**делетепринтер**](deleteprinter.md) для удаления локального принтера.</span><span class="sxs-lookup"><span data-stu-id="e8fab-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="e8fab-123">Приложение должно вызывать [**делетепринтерконнектион**](deleteprinterconnection.md) для удаления подключения к принтеру.</span><span class="sxs-lookup"><span data-stu-id="e8fab-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8fab-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e8fab-124">Requirements</span></span>



| <span data-ttu-id="e8fab-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e8fab-125">Requirement</span></span> | <span data-ttu-id="e8fab-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e8fab-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fab-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8fab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e8fab-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8fab-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8fab-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8fab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e8fab-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8fab-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8fab-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8fab-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8fab-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8fab-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e8fab-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8fab-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8fab-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8fab-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e8fab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e8fab-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8fab-136"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e8fab-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e8fab-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8fab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fab-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e8fab-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e8fab-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="e8fab-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e8fab-140">**аддпринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="e8fab-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="e8fab-141">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="e8fab-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="e8fab-142">**делетепринтер**</span><span class="sxs-lookup"><span data-stu-id="e8fab-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="e8fab-143">**делетепринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="e8fab-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="e8fab-144">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="e8fab-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="e8fab-145">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e8fab-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




