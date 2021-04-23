---
description: Функция Енумпринтеркэй перечисляет подразделы указанного ключа для указанного принтера.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Функция Енумпринтеркэй (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347495"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="5d53b-103">Функция Енумпринтеркэй</span><span class="sxs-lookup"><span data-stu-id="5d53b-103">EnumPrinterKey function</span></span>

<span data-ttu-id="5d53b-104">Функция **енумпринтеркэй** перечисляет подразделы указанного ключа для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="5d53b-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="5d53b-105">Данные принтера хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="5d53b-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="5d53b-106">При перечислении данных принтера не следует вызывать функции реестра, которые могут изменить данные.</span><span class="sxs-lookup"><span data-stu-id="5d53b-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d53b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d53b-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="5d53b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d53b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d53b-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53b-110">Описатель принтера, для которого функция перечисляет подразделы.</span><span class="sxs-lookup"><span data-stu-id="5d53b-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="5d53b-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="5d53b-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="5d53b-112">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53b-113">Указатель на строку, завершающуюся нулем, которая указывает ключ, содержащий подразделы для перечисления.</span><span class="sxs-lookup"><span data-stu-id="5d53b-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="5d53b-114">Используйте символ обратной косой черты в \\ качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="5d53b-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="5d53b-115">**Енумпринтеркэй** перечисляет все подразделы ключа, но не перечисляет подразделы этих подразделов.</span><span class="sxs-lookup"><span data-stu-id="5d53b-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="5d53b-116">Если *пкэйнаме* является пустой строкой (""), **енумпринтеркэй** перечисляет ключ верхнего уровня для принтера.</span><span class="sxs-lookup"><span data-stu-id="5d53b-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="5d53b-117">Если *пкэйнаме* имеет **значение NULL**, **енумпринтеркэй** возвращает ошибку \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="5d53b-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="5d53b-118">*псубкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53b-119">Указатель на буфер, который получает массив имен подразделов, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="5d53b-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="5d53b-120">Массив завершается двумя символами NULL.</span><span class="sxs-lookup"><span data-stu-id="5d53b-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="5d53b-121">*кбсубкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53b-122">Размер (в байтах) буфера, на который указывает *псубкэй*.</span><span class="sxs-lookup"><span data-stu-id="5d53b-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="5d53b-123">Если для *кбсубкэй* задано значение 0, то параметр *пкбсубкэй* возвращает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="5d53b-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="5d53b-124">*пкбсубкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53b-125">Указатель на переменную, которая получает число байтов, полученных в буфере *псубкэй* .</span><span class="sxs-lookup"><span data-stu-id="5d53b-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="5d53b-126">Если размер буфера, указанный параметром *кбсубкэй* , слишком мал, функция возвращает ошибку \_ больше \_ данных, а *пкбсубкэй* указывает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="5d53b-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d53b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d53b-127">Return value</span></span>

<span data-ttu-id="5d53b-128">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5d53b-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5d53b-129">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="5d53b-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="5d53b-130">Если *пкэйнаме* не существует, возвращаемое значение — " \_ файл ошибки \_ не \_ найден".</span><span class="sxs-lookup"><span data-stu-id="5d53b-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d53b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d53b-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d53b-132">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="5d53b-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5d53b-133">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="5d53b-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5d53b-134">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="5d53b-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d53b-135">Требования</span><span class="sxs-lookup"><span data-stu-id="5d53b-135">Requirements</span></span>



| <span data-ttu-id="5d53b-136">Требование</span><span class="sxs-lookup"><span data-stu-id="5d53b-136">Requirement</span></span> | <span data-ttu-id="5d53b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5d53b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d53b-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d53b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5d53b-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d53b-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d53b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5d53b-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d53b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d53b-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5d53b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d53b-143"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d53b-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5d53b-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d53b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d53b-145"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d53b-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5d53b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5d53b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d53b-147"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5d53b-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5d53b-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5d53b-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d53b-149">**Енумпринтеркэйв** (Юникод) и **енумпринтеркэйа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5d53b-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="5d53b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d53b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d53b-151">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5d53b-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5d53b-152">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="5d53b-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5d53b-153">**делетепринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="5d53b-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="5d53b-154">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="5d53b-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="5d53b-155">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="5d53b-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="5d53b-156">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="5d53b-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




