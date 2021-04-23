---
description: Функция Енумформс перечисляет формы, поддерживаемые указанным принтером.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Функция Енумформс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345302"
---
# <a name="enumforms-function"></a><span data-ttu-id="61d62-103">Функция Енумформс</span><span class="sxs-lookup"><span data-stu-id="61d62-103">EnumForms function</span></span>

<span data-ttu-id="61d62-104">Функция **енумформс** перечисляет формы, поддерживаемые указанным принтером.</span><span class="sxs-lookup"><span data-stu-id="61d62-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d62-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61d62-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="61d62-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61d62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d62-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61d62-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-108">Обработчик для принтера, для которого необходимо перечислить формы.</span><span class="sxs-lookup"><span data-stu-id="61d62-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="61d62-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="61d62-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="61d62-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61d62-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-111">Указывает версию структуры, на которую указывает *пформ* .</span><span class="sxs-lookup"><span data-stu-id="61d62-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="61d62-112">Это значение должно быть равно 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="61d62-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="61d62-113">*пформ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61d62-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-114">Указатель на одну или несколько [**структур \_ сведений о форме \_ 1**](form-info-1.md) или в одну или несколько структур [**\_ сведений о форме \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="61d62-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="61d62-115">Все структуры будут иметь одинаковый уровень.</span><span class="sxs-lookup"><span data-stu-id="61d62-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="61d62-116">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61d62-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-117">Задает размер (в байтах) буфера, на который *пформ* указывает.</span><span class="sxs-lookup"><span data-stu-id="61d62-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="61d62-118">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61d62-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-119">Указатель на переменную, которая получает число байтов, скопированных в массив, в который *пформ* указывает (если операция выполнена успешно), или требуемое число байтов (в случае сбоя, так как *кббуф* слишком мал).</span><span class="sxs-lookup"><span data-stu-id="61d62-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="61d62-120">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61d62-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61d62-121">Указатель на переменную, которая получает число структур, скопированных в массив, в который *пформ* Points.</span><span class="sxs-lookup"><span data-stu-id="61d62-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d62-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61d62-122">Return value</span></span>

<span data-ttu-id="61d62-123">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="61d62-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="61d62-124">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="61d62-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="61d62-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61d62-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61d62-126">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="61d62-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="61d62-127">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="61d62-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="61d62-128">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="61d62-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="61d62-129">Если вызывающий объект является удаленным, а *уровень* равен 2, то значение **стрингтипе** в возвращенных структурах [**формы \_ info \_**](form-info-2.md) всегда будет **строковым \_ лангпаир**.</span><span class="sxs-lookup"><span data-stu-id="61d62-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="61d62-130">В Windows Vista данные формы, возвращаемые функцией **енумформс** , извлекаются из локального кэша, когда *хпринтер* ссылается на удаленный сервер печати или на принтер, размещенный на сервере печати, и существует по крайней мере одно открытое соединение с принтером на удаленном сервере печати.</span><span class="sxs-lookup"><span data-stu-id="61d62-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="61d62-131">Во всех остальных конфигурациях данные формы запрашиваются с удаленного сервера печати.</span><span class="sxs-lookup"><span data-stu-id="61d62-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d62-132">Требования</span><span class="sxs-lookup"><span data-stu-id="61d62-132">Requirements</span></span>



| <span data-ttu-id="61d62-133">Требование</span><span class="sxs-lookup"><span data-stu-id="61d62-133">Requirement</span></span> | <span data-ttu-id="61d62-134">Значение</span><span class="sxs-lookup"><span data-stu-id="61d62-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d62-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61d62-135">Minimum supported client</span></span><br/> | <span data-ttu-id="61d62-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61d62-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="61d62-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61d62-137">Minimum supported server</span></span><br/> | <span data-ttu-id="61d62-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61d62-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61d62-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61d62-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d62-140"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61d62-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="61d62-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61d62-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="61d62-142"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61d62-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="61d62-143">DLL</span><span class="sxs-lookup"><span data-stu-id="61d62-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61d62-144"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="61d62-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="61d62-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="61d62-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="61d62-146">**Енумформсв** (Юникод) и **енумформса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="61d62-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="61d62-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61d62-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d62-148">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="61d62-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="61d62-149">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="61d62-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="61d62-150">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="61d62-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="61d62-151">**\_Сведения о форме \_ 1**</span><span class="sxs-lookup"><span data-stu-id="61d62-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="61d62-152">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="61d62-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




