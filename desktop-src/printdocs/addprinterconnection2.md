---
description: Добавляет подключение к указанному принтеру для текущего пользователя и задает сведения о подключении.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Функция AddPrinterConnection2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673637"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="45b66-103">Функция AddPrinterConnection2</span><span class="sxs-lookup"><span data-stu-id="45b66-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="45b66-104">Добавляет подключение к указанному принтеру для текущего пользователя и задает сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="45b66-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b66-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45b66-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="45b66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45b66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b66-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45b66-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b66-108">Маркер родительского окна, в котором будет отображаться диалоговое окно, если система печати должна загрузить драйвер принтера с сервера печати для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="45b66-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="45b66-109">*pszName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45b66-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b66-110">Указатель на константную строку с завершающим нулем, указывающую имя принтера, к которому текущий пользователь хочет подключиться.</span><span class="sxs-lookup"><span data-stu-id="45b66-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="45b66-111">*двлевел*</span><span class="sxs-lookup"><span data-stu-id="45b66-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="45b66-112">Версия структуры, на которую указывает *пконнектионинфо*.</span><span class="sxs-lookup"><span data-stu-id="45b66-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="45b66-113">В настоящее время определен только уровень 1, поэтому значение *двлевел* должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="45b66-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="45b66-114">*пконнектионинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45b66-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b66-115">Указатель на структуру [**\_ \_ \_ 1 подключения принтера**](printer-connection-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="45b66-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="45b66-116">Дополнительные сведения об этом параметре см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="45b66-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b66-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45b66-117">Return value</span></span>

<span data-ttu-id="45b66-118">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="45b66-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="45b66-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="45b66-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="45b66-120">Для получения расширенных сведений об ошибках вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="45b66-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="45b66-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45b66-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45b66-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="45b66-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="45b66-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="45b66-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="45b66-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="45b66-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="45b66-125">Когда Windows Vista устанавливает подключение к принтеру, может потребоваться скопировать файлы драйвера принтера с сервера, к которому подключен принтер.</span><span class="sxs-lookup"><span data-stu-id="45b66-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="45b66-126">Если пользователь не имеет разрешения на копирование файлов в соответствующее расположение, функция **AddPrinterConnection2** завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает сообщение об ошибке " \_ отказано в доступе" \_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="45b66-127">Если файлы драйвера принтера должны быть скопированы с сервера печати, но не могут быть автоматически скопированы из-за действующих групповых политик и подключения к ПРИНТЕРу, \_ \_ \_ в *пконнектионинфо->dwFlags* не отображаются никакие диалоговые окна, и вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="45b66-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="45b66-128">Если для отображения заданий печати для этого принтера можно использовать локальный драйвер принтера, а версия локального драйвера не должна совпадать с версией драйвера принтера на сервере, настройте \_ несоответствие подключения к принтеру \_ в *Пконнектионинфо->dwFlags* и назначьте указатель на строковую переменную, содержащую путь к локальному драйверу принтера, в *пконнектионинфо->псздривернаме*.</span><span class="sxs-lookup"><span data-stu-id="45b66-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="45b66-129">Подключение принтера, установленное с помощью вызова **AddPrinterConnection2** , будет перечислено при вызове [**енумпринтерс**](enumprinters.md) с параметром *двтипе* , установленным в значение Printer \_ reenum \_ Connection.</span><span class="sxs-lookup"><span data-stu-id="45b66-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="45b66-130">Версия ANSI этой функции, **AddPrinterConnection2A**, не поддерживается и возвращает **ошибку \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="45b66-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b66-131">Требования</span><span class="sxs-lookup"><span data-stu-id="45b66-131">Requirements</span></span>



| <span data-ttu-id="45b66-132">Требование</span><span class="sxs-lookup"><span data-stu-id="45b66-132">Requirement</span></span> | <span data-ttu-id="45b66-133">Значение</span><span class="sxs-lookup"><span data-stu-id="45b66-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b66-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45b66-134">Minimum supported client</span></span><br/> | <span data-ttu-id="45b66-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45b66-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="45b66-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45b66-136">Minimum supported server</span></span><br/> | <span data-ttu-id="45b66-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45b66-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="45b66-138">Header</span><span class="sxs-lookup"><span data-stu-id="45b66-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b66-139"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45b66-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="45b66-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45b66-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="45b66-141"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45b66-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="45b66-142">DLL</span><span class="sxs-lookup"><span data-stu-id="45b66-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45b66-143"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="45b66-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="45b66-144">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="45b66-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="45b66-145">**AddPrinterConnection2W** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="45b66-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="45b66-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45b66-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b66-147">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="45b66-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="45b66-148">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="45b66-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="45b66-149">**коннекттопринтердлг**</span><span class="sxs-lookup"><span data-stu-id="45b66-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="45b66-150">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="45b66-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="45b66-151">**делетепринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="45b66-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

