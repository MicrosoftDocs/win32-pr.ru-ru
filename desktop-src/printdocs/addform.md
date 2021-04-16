---
description: Функция Аддформ добавляет форму в список доступных форм, которые можно выбрать для указанного принтера.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Функция Аддформ (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693044"
---
# <a name="addform-function"></a><span data-ttu-id="e80a2-103">Функция Аддформ</span><span class="sxs-lookup"><span data-stu-id="e80a2-103">AddForm function</span></span>

<span data-ttu-id="e80a2-104">Функция **аддформ** добавляет форму в список доступных форм, которые можно выбрать для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="e80a2-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e80a2-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="e80a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e80a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80a2-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e80a2-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80a2-108">Маркер принтера, поддерживающий печать с указанной формой.</span><span class="sxs-lookup"><span data-stu-id="e80a2-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="e80a2-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="e80a2-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e80a2-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e80a2-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80a2-111">Уровень структуры, на которую указывает *пформ* .</span><span class="sxs-lookup"><span data-stu-id="e80a2-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="e80a2-112">Это значение должно быть равно 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="e80a2-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e80a2-113">*пформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e80a2-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80a2-114">Указатель на [**\_ информационную структуру формы \_ 1**](form-info-1.md) или [**\_ сведения о форме \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="e80a2-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80a2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e80a2-115">Return value</span></span>

<span data-ttu-id="e80a2-116">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="e80a2-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e80a2-117">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e80a2-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e80a2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e80a2-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e80a2-119">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="e80a2-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e80a2-120">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="e80a2-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e80a2-121">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="e80a2-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e80a2-122">Приложение может определить, какие формы доступны для принтера, вызвав функцию [**енумформс**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="e80a2-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="e80a2-123">Если *пформ* указывает на [**\_ сведения о форме \_ 2**](form-info-2.md), то **аддформ** завершится ошибкой, если либо форма с указанным именем уже существует, либо значение *пкэйворд* структуры уже существует.</span><span class="sxs-lookup"><span data-stu-id="e80a2-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80a2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e80a2-124">Requirements</span></span>



| <span data-ttu-id="e80a2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e80a2-125">Requirement</span></span> | <span data-ttu-id="e80a2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e80a2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80a2-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e80a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e80a2-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e80a2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e80a2-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e80a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e80a2-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e80a2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e80a2-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e80a2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80a2-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e80a2-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e80a2-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e80a2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e80a2-134"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e80a2-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e80a2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e80a2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80a2-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80a2-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e80a2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e80a2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80a2-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e80a2-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e80a2-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="e80a2-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e80a2-140">**енумформс**</span><span class="sxs-lookup"><span data-stu-id="e80a2-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="e80a2-141">**\_Сведения о форме \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e80a2-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="e80a2-142">**\_Сведения о форме \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e80a2-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="e80a2-143">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="e80a2-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




