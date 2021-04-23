---
description: Функция Енумпринтерс перечисляет доступные принтеры, серверы печати, домены или поставщики печати.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Функция Енумпринтерс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909588"
---
# <a name="enumprinters-function"></a><span data-ttu-id="2f4e5-103">Функция Енумпринтерс</span><span class="sxs-lookup"><span data-stu-id="2f4e5-103">EnumPrinters function</span></span>

<span data-ttu-id="2f4e5-104">Функция **енумпринтерс** перечисляет доступные принтеры, серверы печати, домены или поставщики печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f4e5-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="2f4e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f4e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4e5-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-108">Типы объектов печати, которые должна перечислять функция.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="2f4e5-109">Это значение может быть одним или несколькими следующими значениями.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="2f4e5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4e5-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="2f4e5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4e5-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="2f4e5-112"><dt>**\_локальный принтер перечисление \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="2f4e5-113">Если \_ \_ флаг имени перечисления принтера не передается, функция игнорирует параметр *Name* и перечисляет локально установленные принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="2f4e5-114">Если \_ \_ также передается имя перечисления принтера, функция перечисляет локальные принтеры по *имени*.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="2f4e5-115"><dt>**\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="2f4e5-116">Функция перечисляет принтер, определенный по *имени*.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="2f4e5-117">Это может быть сервер, домен или поставщик услуг печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="2f4e5-118">Если *Name* имеет **значение NULL**, функция перечисляет доступные поставщики печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="2f4e5-119"><dt>**\_перечисление общих принтеров \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="2f4e5-120">Функция перечисляет принтеры, имеющие общий атрибут.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="2f4e5-121">Не может использоваться в изоляции; Используйте операцию или для объединения с другим \_ типом ПЕРЕЧИСЛЕНИЯ принтера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="2f4e5-122"><dt>**Перечисление подключений к ПРИНТЕРАм \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="2f4e5-123">Функция перечисляет список принтеров, к которым пользователь сделал предыдущие соединения.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="2f4e5-124"><dt>**\_сеть перечисление принтеров \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="2f4e5-125">Функция перечисляет сетевые принтеры в домене компьютера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="2f4e5-126">Это значение допустимо, только если *уровень* равен 1.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="2f4e5-127"><dt>**\_Удаленный перечисление принтеров \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="2f4e5-128">Функция перечисляет сетевые принтеры и серверы печати в домене компьютера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="2f4e5-129">Это значение допустимо, только если *уровень* равен 1.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="2f4e5-130"><dt>**Категория перечисления ПРИНТЕРов, \_ \_ \_ трехмерная**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="2f4e5-131">Функция перечисляет только объемные принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="2f4e5-132"><dt>**\_Категория ПЕРЕЧИСЛЕНИЯ принтеров \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="2f4e5-133">Функция перечисляет все устройства печати, включая 3D-принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="2f4e5-134">Если *уровень* равен 4, можно использовать только \_ Локальные константы "перечисление принтера" \_ и " \_ перечисление принтера" \_ .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="2f4e5-135">устройства с 3D-печатью не перечисляются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="2f4e5-136">Чтобы перечислить только объемные принтеры, необходимо включить обе **категории для перечисления принтеров \_ \_ \_ 3D** и **Printer \_ Enum \_ локальный** .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="2f4e5-137">Чтобы включить 3D-принтеры вместе со всеми другими локальными принтерами, используйте **\_ Перечисление \_ категории \_ все** и **\_ \_ Локальное перечисление принтеров локальный**.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="2f4e5-138">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-139">Если *уровень* равен 1, *Флаги* содержат \_ имя перечисления принтера \_ , *а имя* не **равно NULL**, то *Name* — это указатель на строку, завершающуюся нулем, которая указывает имя объекта для перечисления.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="2f4e5-140">Эта строка может быть именем сервера, домена или поставщика услуг печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="2f4e5-141">Если *уровень* равен 1, *Флаги* содержат \_ имя перечисления принтера \_ , а *Name* — **null**, функция перечисляет доступные поставщики печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="2f4e5-142">Если *уровень* равен 1, *Флаги* содержат \_ УДАЛЕНное перечисление принтеров \_ , а *Name* имеет **значение NULL**, функция перечисляет принтеры в домене пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="2f4e5-143">Если *Level* имеет значение 2 или 5, то *Name* — это указатель на строку, завершающуюся нулем, которая указывает имя сервера, чьи принтеры необходимо перечислить.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="2f4e5-144">Если эта строка имеет **значение NULL**, функция перечисляет принтеры, установленные на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="2f4e5-145">Если *уровень* равен 4, *имя* должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="2f4e5-146">Функция всегда запрашивается на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="2f4e5-147">Если параметр *Name* имеет **значение NULL**, при установке *флагов* на принтер перечисление локального принтера перечисление \_ \_ \| \_ \_ подключений перечисляет принтеры, установленные на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="2f4e5-148">К этим принтерам относятся те, которые физически подключены к локальному компьютеру, а также удаленные принтеры, к которым подключено сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="2f4e5-149">Если параметр *Name* имеет **значение NOT NULL**, установка *флагов* на принтер перечисление \_ \_ локального \| принтера \_ \_ перечисляет локальные принтеры, установленные на *имени* сервера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="2f4e5-150">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-151">Тип структур данных, на которые указывает *ппринтеренум*.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="2f4e5-152">Допустимые значения: 1, 2, 4 и 5, соответствующие структурам данных [**принтера \_ \_ 1**](printer-info-1.md), [**\_ сведения о \_ принтере**](printer-info-2.md) , [**сведения о принтере \_ \_ 4**](printer-info-4.md)и [**\_ сведения о принтере \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="2f4e5-153">Это значение может быть равно 1, 2, 4 или 5.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="2f4e5-154">*ппринтеренум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-155">Указатель на буфер, который получает массив [**сведений о принтере \_ \_ 1**](printer-info-1.md), [**\_ сведения о принтере \_**](printer-info-2.md), сведения о [**принтере \_ \_ 4**](printer-info-4.md)или [**\_ сведения о принтере \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="2f4e5-156">Каждая структура содержит данные, описывающие доступный объект Print.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="2f4e5-157">Если *уровень* равен 1, массив содержит структуры [**« \_ \_ 1**](printer-info-1.md) », «принтер».</span><span class="sxs-lookup"><span data-stu-id="2f4e5-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="2f4e5-158">Если *уровень* равен 2, массив содержит структуры [**" \_ сведения \_ о принтере 2**](printer-info-2.md) ".</span><span class="sxs-lookup"><span data-stu-id="2f4e5-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="2f4e5-159">Если *Level* имеет значение 4, то массив содержит структуры [**Printer \_ info \_ 4**](printer-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="2f4e5-160">Если *Level* имеет значение 5, то массив содержит структуры [**Printer \_ info \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="2f4e5-161">Буфер должен быть достаточно большим, чтобы получать массив структур данных и любые строки или другие данные, к которым она указывает.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="2f4e5-162">Если буфер слишком мал, параметр *пкбнидед* возвращает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="2f4e5-163">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-164">Размер (в байтах) буфера, на который указывает *ппринтеренум*.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="2f4e5-165">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-166">Указатель на значение, которое получает число байтов, скопированных, если функция выполнена, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="2f4e5-167">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4e5-168">Указатель на значение, получающее число структур, которые получает количество [**принтеров \_ \_ 1**](printer-info-1.md), [**\_ сведения о принтере \_ 2**](printer-info-2.md) , [**\_ сведения о принтере \_ 4**](printer-info-4.md)или [**\_ сведения о принтере \_ 5**](printer-info-5.md) , возвращаемые функцией в массиве, на который указывает *ппринтеренум* .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4e5-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f4e5-169">Return value</span></span>

<span data-ttu-id="2f4e5-170">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2f4e5-171">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4e5-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f4e5-172">Remarks</span></span>

<span data-ttu-id="2f4e5-173">Не вызывайте этот метод в [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="2f4e5-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="2f4e5-174">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2f4e5-175">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2f4e5-176">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2f4e5-177">Если **енумпринтерс** возвращает структуру [**Printer \_ info \_ 1**](printer-info-1.md) , в которой \_ указан контейнер перечисления принтеров \_ , это означает, что имеется иерархия объектов принтера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="2f4e5-178">Приложение может перечислить иерархию, вызвав **енумпринтерс** еще раз, указав в качестве *имени* значение элемента **pName** в структуре " **\_ сведения о принтере \_ 1** ".</span><span class="sxs-lookup"><span data-stu-id="2f4e5-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="2f4e5-179">Функция **енумпринтерс** не получает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="2f4e5-180">Если в массиве, на который указывает *ппринтеренум*, возвращаются структуры с [**\_ информацией о принтерах \_ 2**](printer-info-2.md) , их члены *псекуритидескриптор* будут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="2f4e5-181">Чтобы получить сведения о принтере по умолчанию, вызовите [**жетдефаултпринтер**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="2f4e5-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="2f4e5-182">Структура [**Printer \_ info \_ 4**](printer-info-4.md) обеспечивает простой и быстрый способ получения имен принтеров, установленных на локальном компьютере, а также удаленных подключений, которые пользователь установил.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="2f4e5-183">Когда **енумпринтерс** вызывается со структурой данных **Printer \_ \_ 4** , эта функция запрашивает в реестре указанные сведения, а затем сразу же возвращает.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="2f4e5-184">Это отличается от поведения **енумпринтерс** при вызове с другими уровнями **\_ \_ \* *структуры данных принтера. В частности, при* вызове _ енумпринтерс** со структурой данных уровня 2 (принтер) он выполняет вызов [**опенпринтер**](openprinter.md) для каждого удаленного соединения.[**\_ \_**](printer-info-2.md)</span><span class="sxs-lookup"><span data-stu-id="2f4e5-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="2f4e5-185">Если удаленное подключение не работает или удаленный сервер больше не существует или удаленный принтер больше не существует, функция должна дождаться истечения времени ожидания RPC и, следовательно, вызвать сбой вызова **опенпринтер** .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="2f4e5-186">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-186">This can take a while.</span></span> <span data-ttu-id="2f4e5-187">Передача структуры **" \_ сведения \_ о принтере 4** " позволяет приложению получить минимально необходимую информацию. Если требуется более подробная информация, можно выполнить следующий вызов **енумпринтерс** уровня 2.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="2f4e5-188">**Windows Vista:** Данные принтера, возвращаемые функцией **енумпринтерс** , извлекаются из локального кэша, когда значение *Level* равно 4.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="2f4e5-189">В следующей таблице показаны выходные данные **енумпринтерс** для различных значений *флагов* , если параметр *Level* имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="2f4e5-190">В столбце "параметр *имени* " таблицы следует подставить соответствующее имя для поставщика печати, домена и компьютера.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="2f4e5-191">Например, для «поставщика печати» можно использовать имя поставщика сетевых принтеров или имя локального поставщика печати.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="2f4e5-192">Чтобы получить имена поставщиков печати, вызовите **енумпринтерс** с параметром *Name* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="2f4e5-193">Параметр *flags*</span><span class="sxs-lookup"><span data-stu-id="2f4e5-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="2f4e5-194">Параметр *Name*</span><span class="sxs-lookup"><span data-stu-id="2f4e5-194">*Name* parameter</span></span>                            | <span data-ttu-id="2f4e5-195">Результат</span><span class="sxs-lookup"><span data-stu-id="2f4e5-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4e5-196">\_Перечисление ЛОКАЛЬНЫХ принтеров \_ ( \_ без \_ имени перечисления принтера)</span><span class="sxs-lookup"><span data-stu-id="2f4e5-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="2f4e5-197">Параметр *Name* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="2f4e5-198">Все локальные принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="2f4e5-199">\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="2f4e5-200">"Поставщик печати"</span><span class="sxs-lookup"><span data-stu-id="2f4e5-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="2f4e5-201">Все доменные имена</span><span class="sxs-lookup"><span data-stu-id="2f4e5-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="2f4e5-202">\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="2f4e5-203">"Поставщик печати! Поддомен</span><span class="sxs-lookup"><span data-stu-id="2f4e5-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="2f4e5-204">Все принтеры и серверы печати в домене компьютера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="2f4e5-205">\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="2f4e5-206">"Поставщик печати! \\ \\ Машине</span><span class="sxs-lookup"><span data-stu-id="2f4e5-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="2f4e5-207">Все общие принтеры на \\ \\ компьютере</span><span class="sxs-lookup"><span data-stu-id="2f4e5-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="2f4e5-208">\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="2f4e5-209">Пустая строка ""</span><span class="sxs-lookup"><span data-stu-id="2f4e5-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="2f4e5-210">Все локальные принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="2f4e5-211">\_имя ПЕРЕЧИСЛЕНИЯ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="2f4e5-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-212">**NULL**</span></span><br/>                         | <span data-ttu-id="2f4e5-213">Все поставщики печати в домене компьютера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="2f4e5-214">Перечисление подключений к ПРИНТЕРАм \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="2f4e5-215">Параметр *Name* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="2f4e5-216">Все подключенные удаленные принтеры</span><span class="sxs-lookup"><span data-stu-id="2f4e5-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="2f4e5-217">\_сеть перечисление принтеров \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="2f4e5-218">Параметр *Name* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="2f4e5-219">Все принтеры в домене компьютера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="2f4e5-220">\_Удаленный перечисление принтеров \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="2f4e5-221">Пустая строка ""</span><span class="sxs-lookup"><span data-stu-id="2f4e5-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="2f4e5-222">Все принтеры и серверы печати в домене компьютера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="2f4e5-223">\_Удаленный перечисление принтеров \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="2f4e5-224">"Поставщик печати"</span><span class="sxs-lookup"><span data-stu-id="2f4e5-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="2f4e5-225">То же, что и \_ имя ПЕРЕЧИСЛЕНИЯ принтера \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="2f4e5-226">\_Удаленный перечисление принтеров \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="2f4e5-227">"Поставщик печати! Поддомен</span><span class="sxs-lookup"><span data-stu-id="2f4e5-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="2f4e5-228">Все принтеры и серверы печати в домене компьютера, независимо от указанного *домена* .</span><span class="sxs-lookup"><span data-stu-id="2f4e5-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="2f4e5-229">Категория перечисления ПРИНТЕРов, \_ \_ \_ трехмерная</span><span class="sxs-lookup"><span data-stu-id="2f4e5-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="2f4e5-230">Параметр *Name* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="2f4e5-231">Перечисляются только объемные принтеры.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="2f4e5-232">\_Категория ПЕРЕЧИСЛЕНИЯ принтеров \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f4e5-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="2f4e5-233">Параметр *Name* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="2f4e5-234">3D-принтеры перечисляются вместе со всеми остальными принтерами.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="2f4e5-235">Требования</span><span class="sxs-lookup"><span data-stu-id="2f4e5-235">Requirements</span></span>



| <span data-ttu-id="2f4e5-236">Требование</span><span class="sxs-lookup"><span data-stu-id="2f4e5-236">Requirement</span></span> | <span data-ttu-id="2f4e5-237">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4e5-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4e5-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f4e5-238">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4e5-239">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f4e5-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-240">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4e5-241">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f4e5-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f4e5-242">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2f4e5-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f4e5-243"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2f4e5-244">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f4e5-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f4e5-245"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2f4e5-246">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4e5-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f4e5-247"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2f4e5-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2f4e5-248">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2f4e5-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f4e5-249">**Енумпринтерсв** (Юникод) и **енумпринтерса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2f4e5-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="2f4e5-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f4e5-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4e5-251">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="2f4e5-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-252">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="2f4e5-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-253">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-254">**делетепринтер**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-255">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-256">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-257">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-258">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-259">**\_Сведения о принтере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="2f4e5-260">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="2f4e5-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

