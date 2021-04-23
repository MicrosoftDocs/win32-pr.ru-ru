---
description: Функция Делетепорт отображает диалоговое окно, позволяющее пользователю удалить имя порта.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Функция Делетепорт (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265352"
---
# <a name="deleteport-function"></a><span data-ttu-id="5969c-103">Функция Делетепорт</span><span class="sxs-lookup"><span data-stu-id="5969c-103">DeletePort function</span></span>

<span data-ttu-id="5969c-104">Функция **делетепорт** отображает диалоговое окно, позволяющее пользователю удалить имя порта.</span><span class="sxs-lookup"><span data-stu-id="5969c-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5969c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5969c-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="5969c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5969c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5969c-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5969c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5969c-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, для которого должен быть удален порт.</span><span class="sxs-lookup"><span data-stu-id="5969c-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="5969c-109">Если этот параметр имеет **значение NULL**, локальный порт удаляется.</span><span class="sxs-lookup"><span data-stu-id="5969c-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="5969c-110">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5969c-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5969c-111">Маркер родительского окна диалогового окна удаления порта.</span><span class="sxs-lookup"><span data-stu-id="5969c-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5969c-112">*ппортнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5969c-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5969c-113">Указатель на строку, завершающуюся нулем, которая указывает имя порта, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="5969c-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5969c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5969c-114">Return value</span></span>

<span data-ttu-id="5969c-115">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="5969c-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5969c-116">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5969c-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5969c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5969c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5969c-118">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="5969c-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5969c-119">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="5969c-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5969c-120">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="5969c-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5969c-121">Приложение может получить имена допустимых портов, вызвав функцию [**енумпортс**](enumports.md) .</span><span class="sxs-lookup"><span data-stu-id="5969c-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="5969c-122">Функция **делетепорт** возвращает ошибку, если в настоящий момент принтер подключен к указанному порту.</span><span class="sxs-lookup"><span data-stu-id="5969c-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="5969c-123">Вызывающая функция **делетепорт** должна иметь доступ к серверу \_ для \_ администрирования доступа к серверу, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="5969c-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="5969c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5969c-124">Requirements</span></span>



| <span data-ttu-id="5969c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5969c-125">Requirement</span></span> | <span data-ttu-id="5969c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5969c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5969c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5969c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5969c-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5969c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5969c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5969c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5969c-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5969c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5969c-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5969c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5969c-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5969c-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5969c-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5969c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5969c-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5969c-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5969c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5969c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5969c-136"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5969c-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5969c-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5969c-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5969c-138">**Делетепортв** (Юникод) и **делетепорта** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5969c-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="5969c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5969c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5969c-140">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5969c-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5969c-141">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="5969c-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5969c-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="5969c-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="5969c-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="5969c-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




