---
description: Функция Аддпорт добавляет имя порта в список поддерживаемых портов. Функция Аддпорт экспортируется монитором порта.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Функция Аддпорт (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912963"
---
# <a name="addport-function"></a><span data-ttu-id="d9891-104">Функция Аддпорт</span><span class="sxs-lookup"><span data-stu-id="d9891-104">AddPort function</span></span>

<span data-ttu-id="d9891-105">Функция **аддпорт** добавляет имя порта в список поддерживаемых портов.</span><span class="sxs-lookup"><span data-stu-id="d9891-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="d9891-106">Функция **аддпорт** экспортируется монитором порта.</span><span class="sxs-lookup"><span data-stu-id="d9891-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9891-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9891-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="d9891-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9891-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9891-109">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9891-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9891-110">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="d9891-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="d9891-111">Если этот параметр имеет **значение NULL**, то порт является локальным.</span><span class="sxs-lookup"><span data-stu-id="d9891-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-112">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9891-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9891-113">Обработчик родительского окна диалогового окна **аддпорт** .</span><span class="sxs-lookup"><span data-stu-id="d9891-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-114">*пмониторнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9891-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9891-115">Указатель на строку, завершающуюся нулем, которая указывает монитор, связанный с портом.</span><span class="sxs-lookup"><span data-stu-id="d9891-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9891-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9891-116">Return value</span></span>

<span data-ttu-id="d9891-117">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="d9891-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d9891-118">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d9891-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9891-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9891-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9891-120">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="d9891-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d9891-121">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="d9891-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d9891-122">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="d9891-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d9891-123">Функция **аддпорт** просматривает сеть, чтобы найти существующие порты, и отображает диалоговое окно для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9891-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="d9891-124">Функция **аддпорт** должна проверить имя порта, указанное пользователем, вызвав [**енумпортс**](enumports.md) , чтобы убедиться, что дублирующиеся имена не существуют.</span><span class="sxs-lookup"><span data-stu-id="d9891-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="d9891-125">Вызывающая функция **аддпорт** должна иметь доступ к серверу \_ для \_ администрирования доступа к серверу, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="d9891-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="d9891-126">Чтобы добавить порт без отображения диалогового окна, вызовите функцию **ксквдата** вместо **аддпорт**.</span><span class="sxs-lookup"><span data-stu-id="d9891-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="d9891-127">Дополнительные сведения о **ксквдата** см. в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="d9891-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9891-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d9891-128">Requirements</span></span>



| <span data-ttu-id="d9891-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d9891-129">Requirement</span></span> | <span data-ttu-id="d9891-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d9891-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9891-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9891-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d9891-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9891-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d9891-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9891-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d9891-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9891-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9891-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9891-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9891-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d9891-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9891-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9891-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d9891-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d9891-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9891-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="d9891-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d9891-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d9891-142">**Аддпортв** (Юникод) и **аддпорта** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d9891-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="d9891-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9891-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9891-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="d9891-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d9891-145">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="d9891-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d9891-146">**делетепорт**</span><span class="sxs-lookup"><span data-stu-id="d9891-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="d9891-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="d9891-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="d9891-148">**сетпорт**</span><span class="sxs-lookup"><span data-stu-id="d9891-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




