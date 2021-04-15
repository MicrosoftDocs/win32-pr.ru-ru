---
description: Извлекает сведения об указанном разделе реестра в автономном кусте реестра.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Функция Оркуеринфокэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668946"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="9391f-103">Функция Оркуеринфокэй</span><span class="sxs-lookup"><span data-stu-id="9391f-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="9391f-104">Извлекает сведения об указанном разделе реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="9391f-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9391f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9391f-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="9391f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9391f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9391f-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9391f-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="9391f-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-109">*лпкласс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-110">Указатель на буфер, который получает класс ключа.</span><span class="sxs-lookup"><span data-stu-id="9391f-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="9391f-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-112">*лпккласс* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-113">Указатель на переменную, указывающую размер буфера, на который указывает параметр *лпкласс* в символах.</span><span class="sxs-lookup"><span data-stu-id="9391f-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="9391f-114">Размер должен включать завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="9391f-114">The size should include the terminating null character.</span></span> <span data-ttu-id="9391f-115">При возврате функции эта переменная содержит размер строки класса, которая хранится в буфере.</span><span class="sxs-lookup"><span data-stu-id="9391f-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="9391f-116">Возвращенное число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="9391f-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="9391f-117">Если буфер недостаточно велик, функция возвращает ошибку \_ больше \_ данных, а переменная содержит размер строки в символах без учета завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="9391f-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="9391f-118">Если *лпкласс* имеет **значение NULL**, *лпккласс* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="9391f-119">Если параметр *лпкласс* является допустимым адресом, а параметр *лпккласс* — нет (например, если параметр *лпккласс* имеет **значение NULL**), функция возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="9391f-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-120">*лпксубкэйс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-121">Указатель на переменную, которая получает количество подразделов, содержащихся в указанном ключе.</span><span class="sxs-lookup"><span data-stu-id="9391f-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="9391f-122">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-123">*лпкмакссубкэйлен* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-124">Указатель на переменную, которая получает размер подраздела ключа с самым длинным именем в символах Юникода, не включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="9391f-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="9391f-125">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-126">*лпкмакскласслен* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-127">Указатель на переменную, которая получает размер самой длинной строки, указывающей класс подраздела, в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="9391f-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="9391f-128">Возвращенное число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="9391f-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="9391f-129">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-130">*лпквалуес* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-131">Указатель на переменную, которая получает количество значений, связанных с ключом.</span><span class="sxs-lookup"><span data-stu-id="9391f-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="9391f-132">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-133">*лпкмаксвалуенамелен* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-134">Указатель на переменную, которая получает размер имени длинного значения ключа в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="9391f-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="9391f-135">Размер не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="9391f-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="9391f-136">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-137">*лпкмаксвалуелен* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-138">Указатель на переменную, которая получает размер наиболее длинного компонента данных из значений ключа в байтах.</span><span class="sxs-lookup"><span data-stu-id="9391f-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="9391f-139">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-140">*лпкбсекуритидескриптор* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-141">Указатель на переменную, которая получает размер дескриптора безопасности ключа в байтах.</span><span class="sxs-lookup"><span data-stu-id="9391f-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="9391f-142">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9391f-143">*лпфтластвритетиме* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9391f-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9391f-144">Указатель на структуру [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , которая получает время последней записи.</span><span class="sxs-lookup"><span data-stu-id="9391f-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="9391f-145">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9391f-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="9391f-146">Функция задает элементы структуры [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , чтобы указать время последнего изменения ключа или любой из его записей значений.</span><span class="sxs-lookup"><span data-stu-id="9391f-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9391f-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9391f-147">Return value</span></span>

<span data-ttu-id="9391f-148">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9391f-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9391f-149">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9391f-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9391f-150">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="9391f-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="9391f-151">Если буфер *лпкласс* слишком мал для получения имени класса, функция возвращает данные об ошибке \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9391f-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9391f-152">Требования</span><span class="sxs-lookup"><span data-stu-id="9391f-152">Requirements</span></span>



| <span data-ttu-id="9391f-153">Требование</span><span class="sxs-lookup"><span data-stu-id="9391f-153">Requirement</span></span> | <span data-ttu-id="9391f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="9391f-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9391f-155">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9391f-155">Redistributable</span></span><br/> | <span data-ttu-id="9391f-156">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="9391f-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9391f-157">Header</span><span class="sxs-lookup"><span data-stu-id="9391f-157">Header</span></span><br/>          | <dl> <span data-ttu-id="9391f-158"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="9391f-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9391f-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9391f-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="9391f-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9391f-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9391f-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9391f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9391f-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="9391f-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="9391f-163">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="9391f-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="9391f-164">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="9391f-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="9391f-165">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="9391f-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
