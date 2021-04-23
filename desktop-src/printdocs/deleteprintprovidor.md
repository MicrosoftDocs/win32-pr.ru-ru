---
description: Функция Делетепринтпровидор Удаляет поставщика печати, добавленного функцией Аддпринтпровидор.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Функция Делетепринтпровидор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265351"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="09365-103">Функция Делетепринтпровидор</span><span class="sxs-lookup"><span data-stu-id="09365-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="09365-104">Функция **делетепринтпровидор** Удаляет поставщика печати, добавленного функцией [**аддпринтпровидор**](addprintprovidor.md) .</span><span class="sxs-lookup"><span data-stu-id="09365-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="09365-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09365-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="09365-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09365-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09365-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09365-108">Процессу должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="09365-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="09365-109">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09365-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09365-110">Указатель на строку, завершающуюся нулем, которая указывает среду, из которой должен быть удален поставщик (например, Windows NT x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="09365-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="09365-111">Если этот параметр имеет **значение NULL**, поставщик удаляется из текущей среды вызывающего приложения и клиентского компьютера (не из целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="09365-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="09365-112">Значение **null** является рекомендуемым значением, так как оно обеспечивает максимальную переносимость.</span><span class="sxs-lookup"><span data-stu-id="09365-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="09365-113">*ппринтпровидернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09365-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09365-114">Указатель на строку, завершающуюся нулем, которая указывает имя удаляемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="09365-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09365-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09365-115">Return value</span></span>

<span data-ttu-id="09365-116">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="09365-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="09365-117">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="09365-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="09365-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09365-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09365-119">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="09365-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="09365-120">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="09365-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="09365-121">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="09365-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09365-122">Требования</span><span class="sxs-lookup"><span data-stu-id="09365-122">Requirements</span></span>



| <span data-ttu-id="09365-123">Требование</span><span class="sxs-lookup"><span data-stu-id="09365-123">Requirement</span></span> | <span data-ttu-id="09365-124">Значение</span><span class="sxs-lookup"><span data-stu-id="09365-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09365-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09365-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09365-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="09365-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09365-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09365-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09365-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="09365-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09365-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="09365-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="09365-130"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09365-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="09365-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09365-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="09365-132"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09365-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="09365-133">DLL</span><span class="sxs-lookup"><span data-stu-id="09365-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09365-134"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="09365-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="09365-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="09365-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="09365-136">**Делетепринтпровидорв** (Юникод) и **делетепринтпровидора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="09365-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="09365-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09365-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09365-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="09365-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="09365-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="09365-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="09365-140">**аддпринтпровидор**</span><span class="sxs-lookup"><span data-stu-id="09365-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




