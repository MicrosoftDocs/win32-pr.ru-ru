---
description: Функция Аддмонитор устанавливает монитор локального порта и связывает файлы конфигурации, данных и монитора.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Функция Аддмонитор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081502"
---
# <a name="addmonitor-function"></a><span data-ttu-id="d4831-103">Функция Аддмонитор</span><span class="sxs-lookup"><span data-stu-id="d4831-103">AddMonitor function</span></span>

<span data-ttu-id="d4831-104">Функция **аддмонитор** устанавливает монитор локального порта и связывает файлы конфигурации, данных и монитора.</span><span class="sxs-lookup"><span data-stu-id="d4831-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4831-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4831-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="d4831-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4831-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4831-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4831-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен монитор.</span><span class="sxs-lookup"><span data-stu-id="d4831-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="d4831-109">Для систем, поддерживающих только локальную установку мониторов, эта строка должна иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d4831-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4831-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4831-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4831-111">Версия структуры, на которую указывает *пмониторс* .</span><span class="sxs-lookup"><span data-stu-id="d4831-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="d4831-112">Это значение должно быть равно 2.</span><span class="sxs-lookup"><span data-stu-id="d4831-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="d4831-113">*пмониторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4831-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4831-114">Указатель на структуру [**\_ сведений о мониторе \_ 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="d4831-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="d4831-115">Если элемент **пенвиронмент** структуры *Пмониторс* имеет **значение NULL**, используется текущая среда вызывающего объекта (клиента), а не целевого (сервера).</span><span class="sxs-lookup"><span data-stu-id="d4831-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="d4831-116">Обратите внимание, что вызов завершится ошибкой, если среда не соответствует среде сервера, то есть можно добавить только монитор, написанный для архитектуры сервера.</span><span class="sxs-lookup"><span data-stu-id="d4831-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4831-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4831-117">Return value</span></span>

<span data-ttu-id="d4831-118">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="d4831-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d4831-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d4831-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4831-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4831-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4831-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="d4831-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d4831-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="d4831-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d4831-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="d4831-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d4831-124">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="d4831-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="d4831-125">Прежде чем приложение вызовет функцию **аддмонитор** , все файлы, необходимые для данного монитора, должны быть скопированы в каталог System32.</span><span class="sxs-lookup"><span data-stu-id="d4831-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="d4831-126">Чтобы определить, какие мониторы портов установлены в настоящий момент, вызовите функцию [**енуммониторс**](enummonitors.md) .</span><span class="sxs-lookup"><span data-stu-id="d4831-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="d4831-127">Чтобы удалить монитор, добавленный с помощью **аддмонитор**, вызовите функцию [**делетемонитор**](deletemonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="d4831-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4831-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d4831-128">Requirements</span></span>



| <span data-ttu-id="d4831-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d4831-129">Requirement</span></span> | <span data-ttu-id="d4831-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d4831-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4831-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4831-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d4831-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4831-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4831-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4831-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d4831-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4831-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4831-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4831-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4831-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4831-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d4831-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4831-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4831-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4831-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d4831-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d4831-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4831-140"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d4831-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d4831-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d4831-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d4831-142">**Аддмониторв** (Юникод) и **аддмонитора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d4831-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="d4831-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4831-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4831-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="d4831-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d4831-145">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="d4831-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d4831-146">**делетемонитор**</span><span class="sxs-lookup"><span data-stu-id="d4831-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="d4831-147">**енуммониторс**</span><span class="sxs-lookup"><span data-stu-id="d4831-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="d4831-148">**\_Сведения о мониторе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d4831-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

