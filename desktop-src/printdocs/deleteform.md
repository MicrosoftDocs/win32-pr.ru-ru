---
description: Функция Делетеформ удаляет имя формы из списка поддерживаемых форм.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Функция Делетеформ (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080776"
---
# <a name="deleteform-function"></a><span data-ttu-id="de629-103">Функция Делетеформ</span><span class="sxs-lookup"><span data-stu-id="de629-103">DeleteForm function</span></span>

<span data-ttu-id="de629-104">Функция **делетеформ** удаляет имя формы из списка поддерживаемых форм.</span><span class="sxs-lookup"><span data-stu-id="de629-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="de629-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de629-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="de629-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de629-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de629-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de629-108">Указывает открытый обработчик принтера, с которым должна выполняться эта функция.</span><span class="sxs-lookup"><span data-stu-id="de629-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="de629-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="de629-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="de629-110">*пформнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de629-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de629-111">Указатель на удаляемое имя формы.</span><span class="sxs-lookup"><span data-stu-id="de629-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de629-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de629-112">Return value</span></span>

<span data-ttu-id="de629-113">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="de629-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="de629-114">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="de629-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="de629-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de629-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de629-116">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="de629-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="de629-117">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="de629-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="de629-118">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="de629-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="de629-119">**Делетеформ** может удалять только имена форм, добавленные с помощью функции [**аддформ**](addform.md) .</span><span class="sxs-lookup"><span data-stu-id="de629-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de629-120">Требования</span><span class="sxs-lookup"><span data-stu-id="de629-120">Requirements</span></span>



| <span data-ttu-id="de629-121">Требование</span><span class="sxs-lookup"><span data-stu-id="de629-121">Requirement</span></span> | <span data-ttu-id="de629-122">Значение</span><span class="sxs-lookup"><span data-stu-id="de629-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de629-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de629-123">Minimum supported client</span></span><br/> | <span data-ttu-id="de629-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de629-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de629-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de629-125">Minimum supported server</span></span><br/> | <span data-ttu-id="de629-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de629-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de629-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="de629-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="de629-128"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de629-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="de629-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de629-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="de629-130"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de629-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="de629-131">DLL</span><span class="sxs-lookup"><span data-stu-id="de629-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de629-132"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="de629-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="de629-133">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="de629-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="de629-134">**Делетеформв** (Юникод) и **делетеформа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="de629-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="de629-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de629-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de629-136">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="de629-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="de629-137">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="de629-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="de629-138">**аддформ**</span><span class="sxs-lookup"><span data-stu-id="de629-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="de629-139">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="de629-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




