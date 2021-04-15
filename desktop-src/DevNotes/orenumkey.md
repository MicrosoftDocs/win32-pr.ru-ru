---
description: Перечисляет подразделы указанного открытого раздела реестра в автономном кусте реестра. Функция получает сведения о одном подразделе при каждом вызове.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Функция Оренумкэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648896"
---
# <a name="orenumkey-function"></a><span data-ttu-id="e2e8a-104">Функция Оренумкэй</span><span class="sxs-lookup"><span data-stu-id="e2e8a-104">OREnumKey function</span></span>

<span data-ttu-id="e2e8a-105">Перечисляет подразделы указанного открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="e2e8a-106">Функция получает сведения о одном подразделе при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e8a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2e8a-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="e2e8a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2e8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e8a-109">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-110">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-111">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-112">Индекс извлекаемого подраздела.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="e2e8a-113">Этот параметр должен быть равен нулю для первого вызова функции и затем увеличивается для последующих вызовов.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="e2e8a-114">Поскольку подразделы не упорядочены, каждый новый подраздел будет иметь произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="e2e8a-115">Это означает, что функция может возвращать подразделы в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-116">*лпнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-117">Указатель на буфер, который получает имя подраздела, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="e2e8a-118">Функция копирует в буфер только имя подраздела, а не полную иерархию ключей.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="e2e8a-119">В случае сбоя функции данные не копируются в буфер.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="e2e8a-120">Дополнительные сведения см. в разделе [ограничения размера элементов реестра](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="e2e8a-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-121">*лпкнаме* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-122">Указатель на переменную, указывающую размер буфера, заданного параметром *лпнаме* в **вчарс**.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="e2e8a-123">Этот размер должен включать завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-123">This size should include the terminating null character.</span></span> <span data-ttu-id="e2e8a-124">Если функция завершается с ошибкой, переменная, на которую указывает *лпкнаме* , содержит количество символов, хранящихся в буфере, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-125">*лпкласс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-126">Указатель на буфер, который получает строку класса перечисления, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="e2e8a-127">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-128">*лпккласс* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-129">Указатель на переменную, указывающую размер буфера, заданного параметром *лпкласс* в **вчарс**.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="e2e8a-130">Размер должен включать завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-130">The size should include the terminating null character.</span></span> <span data-ttu-id="e2e8a-131">Если функция выполнена, *лпккласс* содержит количество символов, хранящихся в буфере, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="e2e8a-132">Этот параметр может иметь **значение NULL** , только если *Лпкласс* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e2e8a-133">*лпфтластвритетиме* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e2e8a-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e8a-134">Указатель на структуру [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , которая получает время последнего написания перечисленного подраздела.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="e2e8a-135">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e8a-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2e8a-136">Return value</span></span>

<span data-ttu-id="e2e8a-137">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e2e8a-138">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="e2e8a-139">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="e2e8a-140">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="e2e8a-141">Если буфер *лпнаме* слишком мал для получения имени ключа, функция возвращает данные об ошибке \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e2e8a-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="e2e8a-142">Если нет доступных подразделов, функция возвращает ошибку больше не содержит \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e8a-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2e8a-143">Remarks</span></span>

<span data-ttu-id="e2e8a-144">Чтобы перечислить подразделы, приложение должно сначала вызвать функцию **оренумкэй** с параметром *двиндекс* , для которого установлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="e2e8a-145">Приложение должно увеличить значение параметра *двиндекс* и вызвать **оренумкэй** , пока не будет больше подразделов (то есть функция возвращает ошибку, что больше \_ нет \_ \_ элементов).</span><span class="sxs-lookup"><span data-stu-id="e2e8a-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="e2e8a-146">Приложение может также установить *двиндекс* в индекс последнего подраздела при первом вызове функции и уменьшить индекс до перечисления подраздела с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="e2e8a-147">Чтобы получить индекс последнего подраздела, используйте функцию [**оркуеринфокэй**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .</span><span class="sxs-lookup"><span data-stu-id="e2e8a-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="e2e8a-148">Хотя приложение использует функцию **оренумкэй** , оно не должно вызывать никакие функции реестра вне сети, которые могут изменить перечисленный ключ.</span><span class="sxs-lookup"><span data-stu-id="e2e8a-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e8a-149">Требования</span><span class="sxs-lookup"><span data-stu-id="e2e8a-149">Requirements</span></span>



| <span data-ttu-id="e2e8a-150">Требование</span><span class="sxs-lookup"><span data-stu-id="e2e8a-150">Requirement</span></span> | <span data-ttu-id="e2e8a-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e2e8a-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e8a-152">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e2e8a-152">Redistributable</span></span><br/> | <span data-ttu-id="e2e8a-153">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e2e8a-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="e2e8a-154">Header</span><span class="sxs-lookup"><span data-stu-id="e2e8a-154">Header</span></span><br/>          | <dl> <span data-ttu-id="e2e8a-155"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e8a-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2e8a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e8a-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="e2e8a-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e8a-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e8a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2e8a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e8a-159">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="e2e8a-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="e2e8a-160">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="e2e8a-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="e2e8a-161">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="e2e8a-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="e2e8a-162">**оркуеринфокэй**</span><span class="sxs-lookup"><span data-stu-id="e2e8a-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
