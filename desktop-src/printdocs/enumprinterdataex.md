---
description: Функция Енумпринтердатаекс перечисляет все имена значений и данные для указанного принтера и ключа.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Функция Енумпринтердатаекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815496"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="1e885-103">Функция Енумпринтердатаекс</span><span class="sxs-lookup"><span data-stu-id="1e885-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="1e885-104">Функция **енумпринтердатаекс** перечисляет все имена значений и данные для указанного принтера и ключа.</span><span class="sxs-lookup"><span data-stu-id="1e885-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="1e885-105">Данные принтера хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="1e885-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="1e885-106">При перечислении данных принтера не следует вызывать функции реестра, которые могут изменить данные.</span><span class="sxs-lookup"><span data-stu-id="1e885-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e885-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e885-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="1e885-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e885-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e885-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e885-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-110">Маркер принтера, для которого функция получает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1e885-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="1e885-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="1e885-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1e885-112">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e885-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-113">Указатель на строку, завершающуюся нулем, которая указывает ключ, содержащий значения для перечисления.</span><span class="sxs-lookup"><span data-stu-id="1e885-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="1e885-114">Используйте символ обратной косой черты ( \\ ) в качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="1e885-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="1e885-115">**Енумпринтердатаекс** перечисляет все значения ключа, но не перечисляет значения подразделов указанного ключа.</span><span class="sxs-lookup"><span data-stu-id="1e885-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="1e885-116">Используйте функцию [**енумпринтеркэй**](enumprinterkey.md) для перечисления подразделов.</span><span class="sxs-lookup"><span data-stu-id="1e885-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="1e885-117">Если *пкэйнаме* имеет **значение NULL** или является пустой строкой, **енумпринтердатаекс** возвращает ошибку \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="1e885-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="1e885-118">*пенумвалуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e885-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-119">Указатель на буфер, который получает массив структур [**\_ \_ значений перечислений принтера**](printer-enum-values.md) .</span><span class="sxs-lookup"><span data-stu-id="1e885-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="1e885-120">Каждая структура содержит имя, тип, данные и размеры значения в разделе ключа.</span><span class="sxs-lookup"><span data-stu-id="1e885-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="1e885-121">*кбенумвалуес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e885-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-122">Размер (в байтах) буфера, на который указывает *пкбенумвалуес*.</span><span class="sxs-lookup"><span data-stu-id="1e885-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="1e885-123">Если для *кбенумвалуес* задано значение 0, то параметр *пкбенумвалуес* возвращает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="1e885-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="1e885-124">*пкбенумвалуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e885-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-125">Указатель на переменную, которая получает размер извлеченных данных конфигурации в байтах.</span><span class="sxs-lookup"><span data-stu-id="1e885-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="1e885-126">Если размер буфера, указанный параметром *кбенумвалуес* , слишком мал, функция возвращает ошибку \_ больше \_ данных, а *пкбенумвалуес* указывает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="1e885-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="1e885-127">*пненумвалуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e885-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e885-128">Указатель на переменную, которая получает число структур [**\_ \_ значений перечислений принтера**](printer-enum-values.md) , возвращаемых в *пенумвалуес*.</span><span class="sxs-lookup"><span data-stu-id="1e885-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e885-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e885-129">Return value</span></span>

<span data-ttu-id="1e885-130">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1e885-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1e885-131">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="1e885-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e885-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e885-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1e885-133">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="1e885-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1e885-134">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="1e885-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1e885-135">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="1e885-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1e885-136">**Енумпринтердатаекс** извлекает данные конфигурации принтера, установленные функциями [**сетпринтердатаекс**](setprinterdataex.md) и [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="1e885-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e885-137">Требования</span><span class="sxs-lookup"><span data-stu-id="1e885-137">Requirements</span></span>



| <span data-ttu-id="1e885-138">Требование</span><span class="sxs-lookup"><span data-stu-id="1e885-138">Requirement</span></span> | <span data-ttu-id="1e885-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e885-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e885-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1e885-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e885-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e885-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e885-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1e885-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e885-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e885-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e885-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e885-145"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e885-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1e885-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e885-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e885-147"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e885-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1e885-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1e885-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e885-149"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1e885-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1e885-150">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="1e885-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e885-151">**Енумпринтердатаексв** (Юникод) и **енумпринтердатаекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1e885-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="1e885-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e885-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e885-153">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="1e885-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1e885-154">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="1e885-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1e885-155">**делетепринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="1e885-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1e885-156">**енумпринтеркэй**</span><span class="sxs-lookup"><span data-stu-id="1e885-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="1e885-157">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="1e885-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1e885-158">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="1e885-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1e885-159">**\_значения перечислений принтера \_**</span><span class="sxs-lookup"><span data-stu-id="1e885-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="1e885-160">**сетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="1e885-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="1e885-161">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="1e885-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




