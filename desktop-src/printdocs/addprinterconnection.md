---
description: Функция Аддпринтерконнектион добавляет подключение к указанному принтеру для текущего пользователя.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Функция Аддпринтерконнектион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911183"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="2f8de-103">Функция Аддпринтерконнектион</span><span class="sxs-lookup"><span data-stu-id="2f8de-103">AddPrinterConnection function</span></span>

<span data-ttu-id="2f8de-104">Функция **аддпринтерконнектион** добавляет подключение к указанному принтеру для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f8de-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f8de-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="2f8de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f8de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8de-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f8de-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8de-108">Указатель на строку, завершающуюся нулем, которая указывает имя принтера, к которому текущий пользователь хочет установить соединение.</span><span class="sxs-lookup"><span data-stu-id="2f8de-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8de-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f8de-109">Return value</span></span>

<span data-ttu-id="2f8de-110">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="2f8de-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2f8de-111">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2f8de-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f8de-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f8de-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f8de-113">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="2f8de-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2f8de-114">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="2f8de-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2f8de-115">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="2f8de-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2f8de-116">Когда Windows устанавливает подключение к принтеру, может потребоваться скопировать файлы драйвера принтера на сервер, к которому подключен принтер.</span><span class="sxs-lookup"><span data-stu-id="2f8de-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="2f8de-117">Если пользователь не имеет разрешения на копирование файлов в соответствующее расположение, функция **аддпринтерконнектион** завершается с ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает сообщение об ошибке " \_ отказано в доступе" \_ .</span><span class="sxs-lookup"><span data-stu-id="2f8de-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="2f8de-118">Подключение принтера, установленное с помощью вызова **аддпринтерконнектион** , будет перечислено при вызове [**енумпринтерс**](enumprinters.md) с параметром *двтипе* , установленным в значение Printer \_ reenum \_ Connection.</span><span class="sxs-lookup"><span data-stu-id="2f8de-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8de-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2f8de-119">Requirements</span></span>



| <span data-ttu-id="2f8de-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2f8de-120">Requirement</span></span> | <span data-ttu-id="2f8de-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2f8de-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8de-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f8de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8de-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f8de-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f8de-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f8de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8de-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f8de-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f8de-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2f8de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f8de-127"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f8de-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2f8de-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f8de-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f8de-129"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f8de-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2f8de-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2f8de-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f8de-131"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2f8de-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2f8de-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2f8de-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f8de-133">**Аддпринтерконнектионв** (Юникод) и **аддпринтерконнектиона** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2f8de-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2f8de-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f8de-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8de-135">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="2f8de-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2f8de-136">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="2f8de-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2f8de-137">**коннекттопринтердлг**</span><span class="sxs-lookup"><span data-stu-id="2f8de-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="2f8de-138">**делетепринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="2f8de-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="2f8de-139">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="2f8de-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

