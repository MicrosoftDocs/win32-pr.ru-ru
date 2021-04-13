---
description: Функция Сетформ задает сведения о форме для указанного принтера.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Функция Сетформ (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345282"
---
# <a name="setform-function"></a><span data-ttu-id="47aba-103">Функция Сетформ</span><span class="sxs-lookup"><span data-stu-id="47aba-103">SetForm function</span></span>

<span data-ttu-id="47aba-104">Функция **сетформ** задает сведения о форме для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="47aba-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="47aba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47aba-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="47aba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47aba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47aba-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47aba-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47aba-108">Маркер принтера, для которого задаются сведения о форме.</span><span class="sxs-lookup"><span data-stu-id="47aba-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="47aba-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="47aba-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="47aba-110">*пформнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47aba-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47aba-111">Указатель на строку, завершающуюся нулем, которая указывает имя формы, для которой задаются сведения о форме.</span><span class="sxs-lookup"><span data-stu-id="47aba-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="47aba-112">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47aba-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47aba-113">Версия структуры, на которую указывает *пформ* .</span><span class="sxs-lookup"><span data-stu-id="47aba-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="47aba-114">Это значение должно быть равно 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="47aba-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="47aba-115">*пформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47aba-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47aba-116">Указатель на [**\_ информационную структуру формы \_ 1**](form-info-1.md) или [**\_ сведения о форме \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="47aba-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47aba-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47aba-117">Return value</span></span>

<span data-ttu-id="47aba-118">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="47aba-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="47aba-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="47aba-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="47aba-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47aba-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="47aba-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="47aba-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="47aba-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="47aba-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="47aba-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="47aba-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="47aba-124">**Сетформ** можно вызывать несколько раз для существующей [**\_ информации о форме \_ 2**](form-info-2.md), каждый вызов добавляет дополнительные пары значений **пдисплайнаме** и **влангид** .</span><span class="sxs-lookup"><span data-stu-id="47aba-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="47aba-125">Все версии формы на всех языках получают **Размер** и **имажеаблеареа** значения **формы \_ info \_ 2** в последнем вызове **сетформ**.</span><span class="sxs-lookup"><span data-stu-id="47aba-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="47aba-126">Если вызывающий объект является удаленным и *уровень* равен 2, значение **стрингтипе** в [**форме \_ info \_ 2**](form-info-2.md) не может быть строковым \_ муидлл.</span><span class="sxs-lookup"><span data-stu-id="47aba-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="47aba-127">Требования</span><span class="sxs-lookup"><span data-stu-id="47aba-127">Requirements</span></span>



| <span data-ttu-id="47aba-128">Требование</span><span class="sxs-lookup"><span data-stu-id="47aba-128">Requirement</span></span> | <span data-ttu-id="47aba-129">Значение</span><span class="sxs-lookup"><span data-stu-id="47aba-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47aba-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47aba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="47aba-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47aba-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="47aba-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47aba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="47aba-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47aba-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="47aba-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47aba-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="47aba-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47aba-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="47aba-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47aba-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="47aba-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47aba-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="47aba-138">DLL</span><span class="sxs-lookup"><span data-stu-id="47aba-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47aba-139"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="47aba-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="47aba-140">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="47aba-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="47aba-141">**Сетформв** (Юникод) и **сетформа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="47aba-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="47aba-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47aba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47aba-143">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="47aba-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="47aba-144">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="47aba-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="47aba-145">**Форма**</span><span class="sxs-lookup"><span data-stu-id="47aba-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="47aba-146">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="47aba-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="47aba-147">**\_Сведения о форме \_ 1**</span><span class="sxs-lookup"><span data-stu-id="47aba-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="47aba-148">**\_Сведения о форме \_ 2**</span><span class="sxs-lookup"><span data-stu-id="47aba-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




