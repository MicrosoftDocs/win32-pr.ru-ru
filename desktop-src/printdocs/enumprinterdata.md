---
description: Функция Енумпринтердата перечисляет данные конфигурации для указанного принтера.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Функция Енумпринтердата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264334"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="3112e-103">Функция Енумпринтердата</span><span class="sxs-lookup"><span data-stu-id="3112e-103">EnumPrinterData function</span></span>

<span data-ttu-id="3112e-104">Функция **енумпринтердата** перечисляет данные конфигурации для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="3112e-105">Чтобы получить данные конфигурации в одном вызове, используйте функцию [**енумпринтердатаекс**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="3112e-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3112e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3112e-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="3112e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3112e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3112e-108">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3112e-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-109">Описатель принтера, данные конфигурации которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="3112e-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="3112e-110">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-111">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3112e-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-112">Значение индекса, указывающее извлекаемое значение данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3112e-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="3112e-113">Присвойте этому параметру значение 0 для первого вызова **енумпринтердата** для указанного маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="3112e-114">Затем увеличивайте параметр на один для последующих вызовов, использующих тот же принтер, пока функция не возвратит ошибку больше \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="3112e-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="3112e-115">Дополнительные сведения см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3112e-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="3112e-116">Если вы используете метод, упомянутый в описаниях параметров *кбвалуенаме* и *cbData* , чтобы получить соответствующие значения размера буфера, установив оба этих параметра равными нулю при первом вызове **енумпринтердата** для указанного дескриптора принтера, значение *двиндекс* не имеет значения для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="3112e-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="3112e-117">Задайте *двиндекс* равным нулю при следующем вызове функции **енумпринтердата** , чтобы запустить фактический процесс перечисления.</span><span class="sxs-lookup"><span data-stu-id="3112e-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="3112e-118">Значения данных конфигурации не упорядочены.</span><span class="sxs-lookup"><span data-stu-id="3112e-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="3112e-119">Новые значения будут иметь произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="3112e-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="3112e-120">Это означает, что функция **енумпринтердата** может возвращать значения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="3112e-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-121">*пвалуенаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3112e-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-122">Указатель на буфер, который получает имя значения данных конфигурации, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="3112e-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-123">*кбвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3112e-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-124">Размер (в байтах) буфера, на который указывает *пвалуенаме*.</span><span class="sxs-lookup"><span data-stu-id="3112e-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="3112e-125">Если требуется, чтобы операционная система предустановила достаточный размер буфера, установите для этого параметра и параметра *cbData* значение ноль для первого вызова **енумпринтердата** для указанного маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="3112e-126">Когда функция возвращает значение, переменная, на которую указывает *пкбвалуенаме* , будет содержать размер буфера, достаточно большой для успешного перечисления всех имен значений данных конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-127">*пкбвалуенаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3112e-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-128">Указатель на переменную, которая получает число байтов, хранящихся в буфере, на который указывает *пвалуенаме*.</span><span class="sxs-lookup"><span data-stu-id="3112e-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-129">*птипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3112e-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-130">Указатель на переменную, которая получает код, указывающий тип данных, хранящихся в указанном значении.</span><span class="sxs-lookup"><span data-stu-id="3112e-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="3112e-131">Список возможных кодов типов см. в разделе [типы значений реестра](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="3112e-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="3112e-132">Параметр *птипе* может иметь **значение NULL** , если код типа не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3112e-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-133">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3112e-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-134">Указатель на буфер, который получает значение данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3112e-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="3112e-135">Этот параметр может быть **равен null** , если значение данных конфигурации не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3112e-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-136">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3112e-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-137">Размер (в байтах) буфера, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="3112e-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="3112e-138">Если требуется, чтобы операционная система предустановила достаточный размер буфера, установите для этого параметра и параметра *кбвалуенаме* значение ноль для первого вызова **енумпринтердата** для указанного маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="3112e-139">Когда функция возвращает значение, переменная, на которую указывает *пкбдата* , будет содержать размер буфера, достаточно большой для успешного перечисления всех имен значений данных конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="3112e-140">*пкбдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3112e-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3112e-141">Указатель на переменную, которая получает число байтов, хранящихся в буфере, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="3112e-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="3112e-142">Этот параметр может иметь **значение NULL** , если *PData* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3112e-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3112e-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3112e-143">Return value</span></span>

<span data-ttu-id="3112e-144">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3112e-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3112e-145">Если функция завершается ошибкой, возвращаемое значение является кодом системной ошибки.</span><span class="sxs-lookup"><span data-stu-id="3112e-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="3112e-146">Функция возвращает ошибку \_ \_ , если больше нет \_ значений данных конфигурации для получения указанного маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="3112e-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3112e-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3112e-148">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="3112e-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3112e-149">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="3112e-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3112e-150">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="3112e-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3112e-151">**Енумпринтердата** извлекает данные конфигурации принтера, установленные функцией [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3112e-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="3112e-152">Данные конфигурации принтера состоят из набора именованных и типизированных значений.</span><span class="sxs-lookup"><span data-stu-id="3112e-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="3112e-153">Функция **енумпринтердата** получает одно из этих значений, имя и код типа, каждый раз при вызове.</span><span class="sxs-lookup"><span data-stu-id="3112e-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="3112e-154">Вызовите функцию **енумпринтердата** несколько раз подряд, чтобы получить все значения данных конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="3112e-155">Данные конфигурации принтера хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="3112e-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="3112e-156">При перечислении данных конфигурации принтера следует избегать вызова функций реестра, которые могут изменить эти данные.</span><span class="sxs-lookup"><span data-stu-id="3112e-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="3112e-157">Если требуется, чтобы операционная система предустановила подходящий размер буфера, сначала вызовите **енумпринтердата** с параметрами *кбвалуенаме* и *cbData* , равными нулю, как отмечалось ранее в разделе Parameters.</span><span class="sxs-lookup"><span data-stu-id="3112e-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="3112e-158">Значение *двиндекс* не имеет значения для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="3112e-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="3112e-159">При возврате функции \* *пкбвалуенаме* и \* *пкбдата* будут содержать размеры буфера, которые достаточно велики для перечисления всех имен и значений значений данных конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="3112e-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="3112e-160">При следующем вызове выделяйте имя значения и буферы данных, задайте для *кбвалуенаме* и *cbData* размеры в байтах выделенных буферов и задайте для *двиндекс* значение 0.</span><span class="sxs-lookup"><span data-stu-id="3112e-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="3112e-161">После этого Продолжайте вызывать функцию **енумпринтердата** , увеличивающую *двиндекс* на единицу каждый раз, пока функция не возвратит ошибку больше \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="3112e-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="3112e-162">Требования</span><span class="sxs-lookup"><span data-stu-id="3112e-162">Requirements</span></span>



| <span data-ttu-id="3112e-163">Требование</span><span class="sxs-lookup"><span data-stu-id="3112e-163">Requirement</span></span> | <span data-ttu-id="3112e-164">Значение</span><span class="sxs-lookup"><span data-stu-id="3112e-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3112e-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3112e-165">Minimum supported client</span></span><br/> | <span data-ttu-id="3112e-166">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3112e-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3112e-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3112e-167">Minimum supported server</span></span><br/> | <span data-ttu-id="3112e-168">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3112e-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3112e-169">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3112e-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="3112e-170"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3112e-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3112e-171">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3112e-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="3112e-172"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3112e-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3112e-173">DLL</span><span class="sxs-lookup"><span data-stu-id="3112e-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3112e-174"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3112e-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3112e-175">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3112e-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3112e-176">**Енумпринтердатав** (Юникод) и **енумпринтердатаа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3112e-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="3112e-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3112e-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3112e-178">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="3112e-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3112e-179">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="3112e-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3112e-180">**делетепринтердата**</span><span class="sxs-lookup"><span data-stu-id="3112e-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="3112e-181">**енумпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="3112e-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3112e-182">**жетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="3112e-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="3112e-183">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="3112e-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3112e-184">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="3112e-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="3112e-185">**сетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="3112e-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

