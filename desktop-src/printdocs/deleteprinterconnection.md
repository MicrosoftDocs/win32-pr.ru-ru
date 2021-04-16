---
description: Функция Делетепринтерконнектион удаляет подключение к принтеру, который был установлен с помощью вызова Аддпринтерконнектион или Коннекттопринтердлг.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: Функция Делетепринтерконнектион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712705"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="6adf8-103">Функция Делетепринтерконнектион</span><span class="sxs-lookup"><span data-stu-id="6adf8-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="6adf8-104">Функция **делетепринтерконнектион** удаляет подключение к принтеру, который был установлен с помощью вызова [**аддпринтерконнектион**](addprinterconnection.md) или [**коннекттопринтердлг**](connecttoprinterdlg.md).</span><span class="sxs-lookup"><span data-stu-id="6adf8-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6adf8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6adf8-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="6adf8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6adf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6adf8-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6adf8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6adf8-108">Указатель на строку, завершающуюся нулем, которая указывает имя удаляемого соединения принтера.</span><span class="sxs-lookup"><span data-stu-id="6adf8-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6adf8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6adf8-109">Return value</span></span>

<span data-ttu-id="6adf8-110">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6adf8-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6adf8-111">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6adf8-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6adf8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6adf8-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6adf8-113">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6adf8-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6adf8-114">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="6adf8-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6adf8-115">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="6adf8-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6adf8-116">Функция **делетепринтерконнектион** не удаляет файлы драйвера принтера, которые были скопированы на сервер, к которому подключен принтер.</span><span class="sxs-lookup"><span data-stu-id="6adf8-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="6adf8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6adf8-117">Requirements</span></span>



| <span data-ttu-id="6adf8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6adf8-118">Requirement</span></span> | <span data-ttu-id="6adf8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6adf8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6adf8-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6adf8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6adf8-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6adf8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6adf8-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6adf8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6adf8-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6adf8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6adf8-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6adf8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6adf8-125"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6adf8-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6adf8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6adf8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6adf8-127"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6adf8-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6adf8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6adf8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6adf8-129"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6adf8-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6adf8-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6adf8-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6adf8-131">**Делетепринтерконнектионв** (Юникод) и **делетепринтерконнектиона** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6adf8-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6adf8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6adf8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adf8-133">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6adf8-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6adf8-134">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6adf8-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6adf8-135">**аддпринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="6adf8-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="6adf8-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="6adf8-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="6adf8-137">**коннекттопринтердлг**</span><span class="sxs-lookup"><span data-stu-id="6adf8-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




