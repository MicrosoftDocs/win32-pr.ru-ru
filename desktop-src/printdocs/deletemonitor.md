---
description: Функция Делетемонитор удаляет монитор портов, добавленный функцией Аддмонитор.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Функция Делетемонитор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693041"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="d003b-103">Функция Делетемонитор</span><span class="sxs-lookup"><span data-stu-id="d003b-103">DeleteMonitor function</span></span>

<span data-ttu-id="d003b-104">Функция **делетемонитор** удаляет монитор портов, добавленный функцией [**аддмонитор**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="d003b-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d003b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d003b-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="d003b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d003b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d003b-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d003b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d003b-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, с которого должен быть удален монитор.</span><span class="sxs-lookup"><span data-stu-id="d003b-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="d003b-109">Если этот параметр имеет **значение NULL**, монитор портов удаляется локально.</span><span class="sxs-lookup"><span data-stu-id="d003b-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="d003b-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d003b-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d003b-111">Указатель на строку, завершающуюся нулем, которая указывает среду, из которой должен быть удален монитор (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="d003b-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="d003b-112">Если этот параметр имеет **значение NULL**, монитор удаляется из текущей среды вызывающего приложения и клиентского компьютера (не из целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="d003b-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="d003b-113">*пмониторнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d003b-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d003b-114">Указатель на строку, завершающуюся нулем, которая указывает имя удаляемого монитора.</span><span class="sxs-lookup"><span data-stu-id="d003b-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d003b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d003b-115">Return value</span></span>

<span data-ttu-id="d003b-116">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="d003b-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d003b-117">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d003b-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d003b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d003b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d003b-119">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="d003b-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d003b-120">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="d003b-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d003b-121">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="d003b-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d003b-122">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="d003b-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="d003b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d003b-123">Requirements</span></span>



| <span data-ttu-id="d003b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d003b-124">Requirement</span></span> | <span data-ttu-id="d003b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d003b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d003b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d003b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d003b-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d003b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d003b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d003b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d003b-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d003b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d003b-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d003b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d003b-131"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d003b-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d003b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d003b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d003b-133"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d003b-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d003b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d003b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d003b-135"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d003b-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d003b-136">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d003b-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d003b-137">**Делетемониторв** (Юникод) и **делетемонитора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d003b-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="d003b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d003b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d003b-139">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="d003b-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d003b-140">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="d003b-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d003b-141">**аддмонитор**</span><span class="sxs-lookup"><span data-stu-id="d003b-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

