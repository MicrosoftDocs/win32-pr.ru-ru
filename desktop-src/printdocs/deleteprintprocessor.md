---
description: Функция Делетепринтпроцессор удаляет обработчик печати, добавленный функцией Аддпринтпроцессор.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Функция Делетепринтпроцессор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264340"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="20c09-103">Функция Делетепринтпроцессор</span><span class="sxs-lookup"><span data-stu-id="20c09-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="20c09-104">Функция **делетепринтпроцессор** удаляет обработчик печати, добавленный функцией [**аддпринтпроцессор**](addprintprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="20c09-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c09-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20c09-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="20c09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20c09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c09-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20c09-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c09-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, с которого должен быть удален процессор.</span><span class="sxs-lookup"><span data-stu-id="20c09-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="20c09-109">Если этот параметр имеет **значение NULL**, то обработчик принтера удаляется локально.</span><span class="sxs-lookup"><span data-stu-id="20c09-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="20c09-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20c09-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c09-111">Указатель на строку, завершающуюся нулем, которая указывает среду, из которой должен быть удален процессор (например, Windows NT x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="20c09-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="20c09-112">Если этот параметр имеет **значение NULL**, то процессор удаляется из текущей среды вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="20c09-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="20c09-113">Значение **null** является рекомендуемым значением, так как оно обеспечивает максимальную переносимость.</span><span class="sxs-lookup"><span data-stu-id="20c09-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="20c09-114">*ппринтпроцессорнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20c09-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c09-115">Указатель на строку, завершающуюся нулем, которая указывает имя удаляемого процессора.</span><span class="sxs-lookup"><span data-stu-id="20c09-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c09-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20c09-116">Return value</span></span>

<span data-ttu-id="20c09-117">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="20c09-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="20c09-118">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="20c09-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c09-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20c09-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20c09-120">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="20c09-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="20c09-121">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="20c09-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="20c09-122">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="20c09-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="20c09-123">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="20c09-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c09-124">Требования</span><span class="sxs-lookup"><span data-stu-id="20c09-124">Requirements</span></span>



| <span data-ttu-id="20c09-125">Требование</span><span class="sxs-lookup"><span data-stu-id="20c09-125">Requirement</span></span> | <span data-ttu-id="20c09-126">Значение</span><span class="sxs-lookup"><span data-stu-id="20c09-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c09-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20c09-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20c09-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20c09-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="20c09-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20c09-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20c09-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20c09-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20c09-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20c09-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="20c09-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20c09-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="20c09-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20c09-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="20c09-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20c09-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="20c09-135">DLL</span><span class="sxs-lookup"><span data-stu-id="20c09-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20c09-136"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="20c09-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="20c09-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="20c09-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20c09-138">**Делетепринтпроцессорв** (Юникод) и **делетепринтпроцессора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20c09-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="20c09-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20c09-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c09-140">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="20c09-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="20c09-141">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="20c09-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="20c09-142">**аддпринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="20c09-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

