---
description: Перечисляет значения указанного открытого раздела реестра в автономном кусте реестра. Функция получает сведения для одного значения в указанном ключе каждый раз при вызове функции.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Функция Оренумвалуе (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668561"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="bf0e0-104">Функция Оренумвалуе</span><span class="sxs-lookup"><span data-stu-id="bf0e0-104">OREnumValue function</span></span>

<span data-ttu-id="bf0e0-105">Перечисляет значения указанного открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="bf0e0-106">Функция получает сведения для одного значения в указанном ключе каждый раз при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf0e0-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="bf0e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf0e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0e0-109">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-110">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-111">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-112">Индекс извлекаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="bf0e0-113">Этот параметр должен быть равен нулю для первого вызова функции, а затем увеличиваться для последующих вызовов.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="bf0e0-114">Поскольку значения не упорядочены, любое новое значение будет иметь произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="bf0e0-115">Это означает, что функция может возвращать значения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-116">*лпвалуенаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-117">Указатель на буфер, который получает имя значения в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="bf0e0-118">Размер этого буфера должен быть достаточным для включения завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="bf0e0-119">Дополнительные сведения см. в разделе [ограничения размера элементов реестра](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="bf0e0-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-120">*лпквалуенаме* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-121">Указатель на переменную, указывающую размер буфера, на который указывает параметр *лпвалуенаме* в символах.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="bf0e0-122">Когда функция возвращает значение, переменная получает количество символов, хранящихся в буфере, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-123">*лптипе* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-124">Указатель на переменную, которая получает код, указывающий тип данных, хранящихся в указанном значении.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="bf0e0-125">Список возможных кодов типов см. в разделе [типы значений реестра](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="bf0e0-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="bf0e0-126">Параметр *лптипе* может иметь **значение NULL** , если код типа не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-127">*лпдата* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-128">Указатель на буфер, который получает данные для записи значения.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="bf0e0-129">Если данные не требуются, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="bf0e0-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="bf0e0-130">Если *лпдата* имеет **значение NULL** , а *лпкбдата* не равен **null**, функция сохраняет размер данных в байтах в переменной, на которую указывает *лпкбдата*.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="bf0e0-131">Это позволяет приложению определить лучший способ выделения буфера для данных.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-132">*лпкбдата* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="bf0e0-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0e0-133">Указатель на переменную, указывающую размер буфера, на который указывает параметр *лпдата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="bf0e0-134">Когда функция возвращает значение, переменная получает число байтов, хранящихся в буфере.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="bf0e0-135">Этот параметр может иметь **значение NULL** , только если *Лпдата* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="bf0e0-136">Если данные имеют \_ тип SZ, REG \_ Multi \_ SZ или REG \_ expand \_ SZ, этот размер включает в себя любой завершающий нуль символ или символы.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="bf0e0-137">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="bf0e0-137">For more information, see Remarks.</span></span>

<span data-ttu-id="bf0e0-138">Если буфер, указанный параметром *лпдата* , недостаточно велик для хранения данных, функция возвращает ошибку \_ больше \_ данных и сохраняет требуемый размер буфера в переменной, на которую указывает *лпкбдата*.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="bf0e0-139">В этом случае содержимое *лпдата* не определено.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0e0-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf0e0-140">Return value</span></span>

<span data-ttu-id="bf0e0-141">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bf0e0-142">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="bf0e0-143">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="bf0e0-144">Если буфер *лпдата* слишком мал для получения значения, функция возвращает данные об ошибке \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bf0e0-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0e0-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf0e0-145">Remarks</span></span>

<span data-ttu-id="bf0e0-146">Чтобы перечислить значения, приложение должно сначала вызвать функцию **оренумвалуе** с параметром *двиндекс* , имеющим значение 0.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="bf0e0-147">Приложение должно увеличить *двиндекс* и вызвать функцию **оренумвалуе** до тех пор, пока не будет больше значений (до тех пор, пока функция не вернет ошибку больше \_ \_ \_ элементов).</span><span class="sxs-lookup"><span data-stu-id="bf0e0-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="bf0e0-148">Приложение может также установить *двиндекс* в индекс последнего значения первого вызова функции и уменьшить индекс до перечисления значения с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="bf0e0-149">Чтобы получить индекс последнего значения, используйте функцию [**оркуеринфокэй**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="bf0e0-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="bf0e0-150">При использовании **оренумвалуе** приложение не должно вызывать никаких функций автономного реестра, которые могут изменить запрашиваемый ключ.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="bf0e0-151">Если данные имеют \_ тип SZ, REG \_ Multi \_ SZ или REG \_ expand \_ SZ, строка может быть не сохранена с правильными символами, завершающимися нулем.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="bf0e0-152">Таким образом, даже если функция возвращает ошибку \_ успешного выполнения, приложение должно убедиться, что строка должна завершиться должным образом, прежде чем использовать ее; в противном случае она может перезаписать буфер.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="bf0e0-153">(Обратите внимание, что REG \_ В нескольких \_ SZ строках должно быть два завершающих символа null.)</span><span class="sxs-lookup"><span data-stu-id="bf0e0-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="bf0e0-154">Для определения максимального размера буферов имен и данных используйте функцию [**оркуеринфокэй**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="bf0e0-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0e0-155">Требования</span><span class="sxs-lookup"><span data-stu-id="bf0e0-155">Requirements</span></span>



| <span data-ttu-id="bf0e0-156">Требование</span><span class="sxs-lookup"><span data-stu-id="bf0e0-156">Requirement</span></span> | <span data-ttu-id="bf0e0-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bf0e0-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0e0-158">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bf0e0-158">Redistributable</span></span><br/> | <span data-ttu-id="bf0e0-159">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="bf0e0-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="bf0e0-160">Header</span><span class="sxs-lookup"><span data-stu-id="bf0e0-160">Header</span></span><br/>          | <dl> <span data-ttu-id="bf0e0-161"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0e0-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf0e0-162">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0e0-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="bf0e0-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0e0-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0e0-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf0e0-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0e0-165">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="bf0e0-166">**оренумкэй**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="bf0e0-167">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="bf0e0-168">**оркуеринфокэй**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
