---
description: Функция Клосепринтер закрывает указанный объект принтера.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Функция Клосепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272373"
---
# <a name="closeprinter-function"></a><span data-ttu-id="6631c-103">Функция Клосепринтер</span><span class="sxs-lookup"><span data-stu-id="6631c-103">ClosePrinter function</span></span>

<span data-ttu-id="6631c-104">Функция **клосепринтер** закрывает указанный объект принтера.</span><span class="sxs-lookup"><span data-stu-id="6631c-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6631c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6631c-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="6631c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6631c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6631c-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6631c-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6631c-108">Описатель для закрытого объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="6631c-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="6631c-109">Этот маркер возвращается функцией [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="6631c-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6631c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6631c-110">Return value</span></span>

<span data-ttu-id="6631c-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6631c-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6631c-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6631c-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6631c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6631c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6631c-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6631c-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6631c-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="6631c-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6631c-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="6631c-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6631c-117">Когда функция **клосепринтер** возвращает, *хпринтер* handle является недопустимым независимо от того, была ли функция успешной или неудачной.</span><span class="sxs-lookup"><span data-stu-id="6631c-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="6631c-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="6631c-118">Examples</span></span>

<span data-ttu-id="6631c-119">Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="6631c-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6631c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6631c-120">Requirements</span></span>



| <span data-ttu-id="6631c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6631c-121">Requirement</span></span> | <span data-ttu-id="6631c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6631c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6631c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6631c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6631c-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6631c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6631c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6631c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6631c-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6631c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6631c-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6631c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6631c-128"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6631c-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6631c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6631c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6631c-130"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6631c-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6631c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6631c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6631c-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6631c-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6631c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6631c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6631c-134">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6631c-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6631c-135">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6631c-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6631c-136">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="6631c-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="6631c-137">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="6631c-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




