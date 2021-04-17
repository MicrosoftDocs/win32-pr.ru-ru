---
description: Функция функции-формы получает сведения об указанной форме.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Функция onform (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693240"
---
# <a name="getform-function"></a><span data-ttu-id="3d2ef-103">Функция onform</span><span class="sxs-lookup"><span data-stu-id="3d2ef-103">GetForm function</span></span>

<span data-ttu-id="3d2ef-104">Функция функции- **формы** получает сведения об указанной форме.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d2ef-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="3d2ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2ef-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-108">Маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-108">A handle to the printer.</span></span> <span data-ttu-id="3d2ef-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ef-110">*пформнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-111">Указатель на строку, завершающуюся нулем, которая указывает имя формы.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="3d2ef-112">Чтобы получить имена форм, поддерживаемых принтером, вызовите функцию [**енумформс**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="3d2ef-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ef-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-114">Версия структуры, на которую указывает *пформ* .</span><span class="sxs-lookup"><span data-stu-id="3d2ef-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="3d2ef-115">Это значение должно быть равно 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ef-116">*пформ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-117">Указатель на массив байтов, получающий инициализированную структуру [**Form \_ info \_ 1**](form-info-1.md) или [**Form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="3d2ef-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ef-118">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-119">Размер массива *пформ* в байтах.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ef-120">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2ef-121">Указатель на значение, указывающее число байтов, скопированных при выполнении функции, или число байтов, необходимых, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d2ef-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d2ef-122">Return value</span></span>

<span data-ttu-id="3d2ef-123">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3d2ef-124">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2ef-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d2ef-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3d2ef-126">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3d2ef-127">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3d2ef-128">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3d2ef-129">Если вызывающий объект является удаленным, а *уровень* равен 2, значение **Стрингтипе** возвращаемой [**формы \_ \_ 2**](form-info-2.md) всегда будет строковым \_ лангпаир.</span><span class="sxs-lookup"><span data-stu-id="3d2ef-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2ef-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3d2ef-130">Requirements</span></span>



| <span data-ttu-id="3d2ef-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3d2ef-131">Requirement</span></span> | <span data-ttu-id="3d2ef-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3d2ef-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2ef-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d2ef-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2ef-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3d2ef-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d2ef-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2ef-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d2ef-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3d2ef-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d2ef-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d2ef-138"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d2ef-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d2ef-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3d2ef-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d2ef-140"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d2ef-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3d2ef-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2ef-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2ef-142"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3d2ef-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3d2ef-143">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3d2ef-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d2ef-144">**Жетформв** (Юникод) и a- **Forms** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3d2ef-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="3d2ef-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d2ef-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2ef-146">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="3d2ef-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3d2ef-147">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="3d2ef-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3d2ef-148">**аддформ**</span><span class="sxs-lookup"><span data-stu-id="3d2ef-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="3d2ef-149">**делетеформ**</span><span class="sxs-lookup"><span data-stu-id="3d2ef-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="3d2ef-150">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="3d2ef-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3d2ef-151">**сетформ**</span><span class="sxs-lookup"><span data-stu-id="3d2ef-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




