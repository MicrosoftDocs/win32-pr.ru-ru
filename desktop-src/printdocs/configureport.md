---
description: Функция Конфигурепорт отображает диалоговое окно настройки порта для порта на указанном сервере.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Функция Конфигурепорт (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998463"
---
# <a name="configureport-function"></a><span data-ttu-id="5fc7c-103">Функция Конфигурепорт</span><span class="sxs-lookup"><span data-stu-id="5fc7c-103">ConfigurePort function</span></span>

<span data-ttu-id="5fc7c-104">Функция **конфигурепорт** отображает диалоговое окно настройки порта для порта на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fc7c-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="5fc7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fc7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc7c-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fc7c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc7c-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором существует указанный порт.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="5fc7c-109">Если этот параметр имеет **значение NULL**, то порт является локальным.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="5fc7c-110">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fc7c-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc7c-111">Обработано с родительским окном диалогового окна настройки порта.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5fc7c-112">*ппортнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fc7c-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc7c-113">Указатель на строку, завершающуюся нулем, которая указывает имя порта для настройки.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc7c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fc7c-114">Return value</span></span>

<span data-ttu-id="5fc7c-115">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5fc7c-116">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc7c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fc7c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5fc7c-118">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5fc7c-119">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5fc7c-120">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5fc7c-121">Перед вызовом функции **конфигурепорт** приложение должно вызвать функцию [**енумпортс**](enumports.md) , чтобы определить допустимые имена портов.</span><span class="sxs-lookup"><span data-stu-id="5fc7c-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc7c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5fc7c-122">Requirements</span></span>



| <span data-ttu-id="5fc7c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5fc7c-123">Requirement</span></span> | <span data-ttu-id="5fc7c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5fc7c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc7c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fc7c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc7c-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5fc7c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5fc7c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fc7c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc7c-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5fc7c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5fc7c-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5fc7c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc7c-130"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc7c-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5fc7c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5fc7c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fc7c-132"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fc7c-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5fc7c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc7c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc7c-134"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5fc7c-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5fc7c-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5fc7c-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5fc7c-136">**Конфигурепортв** (Юникод) и **конфигурепорта** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5fc7c-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="5fc7c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fc7c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc7c-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5fc7c-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5fc7c-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="5fc7c-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5fc7c-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="5fc7c-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




