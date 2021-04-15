---
description: Функция Пдхвбопенлог открывает указанный файл журнала для чтения и записи. Эта функция вызывает Пдхопенлог.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: Функция Пдхвбопенлог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545511"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="43c33-104">Функция Пдхвбопенлог</span><span class="sxs-lookup"><span data-stu-id="43c33-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="43c33-105">Функция **пдхвбопенлог** открывает указанный файл журнала для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="43c33-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="43c33-106">Эта функция вызывает [**пдхопенлог**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span><span class="sxs-lookup"><span data-stu-id="43c33-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43c33-107">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="43c33-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="43c33-108">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="43c33-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="43c33-109">Функция Пдхвбопенлог ( \_ ByVal Сзлогфиленаме AS LPCTSTR, \_ ByVal ДВАКЦЕССФЛАГС как DWORD, \_ BYVAL лпдвлогтипе AS Лпдворд, \_ ByVal хкуери как PDH \_ ХКУЕРИ, \_ ByVal Двмакссизе AS DWORD, \_ ByVal SZUSERCAPTION как LPCSTR, \_ ByRef phLog AS PDH \_ HLOG \_ ) как DWORD</span><span class="sxs-lookup"><span data-stu-id="43c33-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="43c33-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43c33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c33-111">*сзлогфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-112">Указатель на строку, указывающую имя открываемого файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="43c33-113">Если файл журнала содержит данные SQL, формат имени файла журнала — **SQL:**_источник_ данных *_!_* _LogFilename_.</span><span class="sxs-lookup"><span data-stu-id="43c33-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="43c33-114">В этом случае значением параметра *лпдвлогтипе* является \_ тип журнала PDH \_ \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="43c33-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="43c33-115">*двакцессфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-116">Тип доступа, который должен быть указан при открытии файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="43c33-117">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="43c33-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="43c33-118">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="43c33-119">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="43c33-120"><dt>**\_доступ на \_ Чтение \_ журнала PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="43c33-121">Файл журнала открыт для операции чтения.</span><span class="sxs-lookup"><span data-stu-id="43c33-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="43c33-122"><dt>**\_доступ на \_ запись в журнал PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="43c33-123">Для операции записи открыт новый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="43c33-124"><dt>**\_доступ для \_ обновления \_ журнала PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="43c33-125">Для операции записи открыт существующий файл журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="43c33-126">Значение, выбранное из предыдущей таблицы, может быть объединено с помощью оператора OR с одним из следующих флагов создания доступа.</span><span class="sxs-lookup"><span data-stu-id="43c33-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="43c33-127">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="43c33-128">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="43c33-129"><dt>**\_ \_ Создание нового журнала \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="43c33-130">Будет создан новый файл журнала с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="43c33-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="43c33-131"><dt>**\_ \_ всегда создавать журнал \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="43c33-132">Создается новый файл журнала с указанным именем, а любой существующий файл журнала с тем же именем удаляется.</span><span class="sxs-lookup"><span data-stu-id="43c33-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="43c33-133"><dt>**\_Журнал PDH \_ открыт \_ существующий**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="43c33-134">Открывается существующий файл журнала с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="43c33-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="43c33-135">Если файл журнала с указанным именем не существует, это значение совпадает с параметром журнал PDH \_ \_ создать \_ новый.</span><span class="sxs-lookup"><span data-stu-id="43c33-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="43c33-136"><dt>**\_Журнал PDH \_ \_ всегда открыт**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="43c33-137">Открывается существующий файл журнала с указанным именем или создается новый файл журнала с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="43c33-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="43c33-138">*лпдвлогтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-139">Указатель на переменную, которая указывает тип открываемого файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="43c33-140">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="43c33-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="43c33-141">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="43c33-142">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="43c33-143"><dt>**\_тип журнала PDH не \_ \_ определен**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="43c33-144">Неопределенный формат файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="43c33-145"><dt>**\_тип журнала PDH ( \_ \_ CSV)**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="43c33-146">Текстовые файлы, содержащие заголовки столбцов в первой строке, и отдельные образцы данных в каждой последующей строке.</span><span class="sxs-lookup"><span data-stu-id="43c33-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="43c33-147"><dt>**\_тип журнала \_ PDH \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="43c33-148">Данные в файле журнала находятся в SQL.</span><span class="sxs-lookup"><span data-stu-id="43c33-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="43c33-149"><dt>**\_тип журнала \_ PDH \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="43c33-150">То же, что и \_ Формат журнала PDH \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="43c33-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="43c33-151"><dt>**\_ \_ двоичный тип журнала PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="43c33-152">Формат двоичного файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-152">Binary log file format.</span></span> <span data-ttu-id="43c33-153">Содержит циклические файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="43c33-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="43c33-154"><dt>**\_монитор для \_ типа \_ журнала PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="43c33-155">Формат файла журнала Perfmon.</span><span class="sxs-lookup"><span data-stu-id="43c33-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="43c33-156">*хкуери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-157">Обработчик запроса.</span><span class="sxs-lookup"><span data-stu-id="43c33-157">Query handle.</span></span> <span data-ttu-id="43c33-158">Этот маркер возвращается функцией [**пдхвбопенкуери**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="43c33-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="43c33-159">Этот параметр может иметь **значение NULL** , если файл журнала должен быть открыт для чтения.</span><span class="sxs-lookup"><span data-stu-id="43c33-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="43c33-160">*двмакссизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-161">Максимальный размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="43c33-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="43c33-162">Это значение используется только в том случае, если файл журнала имеет ограниченный размер или циклический файл журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="43c33-163">*сзусеркаптион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43c33-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-164">Указатель на строку, которая указывает заданный пользователем заголовок файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="43c33-165">Заголовок файла журнала обычно описывает содержимое файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="43c33-166">При открытии существующего файла журнала значение этого параметра игнорируется.</span><span class="sxs-lookup"><span data-stu-id="43c33-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="43c33-167">*флог* \[ в, ссылка\]</span><span class="sxs-lookup"><span data-stu-id="43c33-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="43c33-168">Указатель на буфер, который получает маркер открытого файла журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c33-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43c33-169">Return value</span></span>

<span data-ttu-id="43c33-170">Если функция завершается с ошибкой, она возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="43c33-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="43c33-171">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="43c33-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="43c33-172">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="43c33-172">The following are possible values.</span></span>



| <span data-ttu-id="43c33-173">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43c33-173">Return code</span></span>                                                                                                | <span data-ttu-id="43c33-174">Описание</span><span class="sxs-lookup"><span data-stu-id="43c33-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43c33-175"><dt>**\_недостаточный \_ Размер буфера PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="43c33-176">Запрошенные данные больше, чем указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="43c33-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="43c33-177">Не удалось вернуть запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="43c33-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="43c33-178"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="43c33-179">Один или несколько буферов строк имеют неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="43c33-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="43c33-180"><dt>**\_Недопустимый \_ маркер PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="43c33-181">Этот маркер не является допустимым объектом PDH.</span><span class="sxs-lookup"><span data-stu-id="43c33-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="43c33-182"><dt>**\_ \_ \_ Ошибка при открытии файла журнала PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="43c33-183">Не удалось открыть указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="43c33-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="43c33-184"><dt>**\_файл PDH \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="43c33-185">Не удалось найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="43c33-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="43c33-186">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43c33-186">Remarks</span></span>

<span data-ttu-id="43c33-187">При использовании этой функции для записи данных о производительности в файл журнала сначала необходимо открыть запрос с помощью [**пдхвбопенкуери**](pdhvbopenquery.md).</span><span class="sxs-lookup"><span data-stu-id="43c33-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="43c33-188">В настоящий момент должен быть открытый запрос, и перед вызовом этой функции необходимо добавить в него нужные счетчики.</span><span class="sxs-lookup"><span data-stu-id="43c33-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="43c33-189">Обратите внимание, что файлы журнала в формате PerfMon можно открывать только для чтения.</span><span class="sxs-lookup"><span data-stu-id="43c33-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c33-190">Требования</span><span class="sxs-lookup"><span data-stu-id="43c33-190">Requirements</span></span>



| <span data-ttu-id="43c33-191">Требование</span><span class="sxs-lookup"><span data-stu-id="43c33-191">Requirement</span></span> | <span data-ttu-id="43c33-192">Значение</span><span class="sxs-lookup"><span data-stu-id="43c33-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43c33-193">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43c33-193">Minimum supported client</span></span><br/> | <span data-ttu-id="43c33-194">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43c33-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43c33-195">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43c33-195">Minimum supported server</span></span><br/> | <span data-ttu-id="43c33-196">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43c33-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43c33-197">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43c33-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="43c33-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="43c33-199">DLL</span><span class="sxs-lookup"><span data-stu-id="43c33-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43c33-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43c33-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c33-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43c33-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c33-202">**пдхопенлог**</span><span class="sxs-lookup"><span data-stu-id="43c33-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="43c33-203">**пдхвбжетлогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="43c33-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="43c33-204">**пдхвбупдателог**</span><span class="sxs-lookup"><span data-stu-id="43c33-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

