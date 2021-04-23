---
description: Извлекает тип и данные для указанного значения реестра в автономном кусте реестра.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Функция Оржетвалуе (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648764"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="d2a95-103">Функция Оржетвалуе</span><span class="sxs-lookup"><span data-stu-id="d2a95-103">ORGetValue function</span></span>

<span data-ttu-id="d2a95-104">Извлекает тип и данные для указанного значения реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="d2a95-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2a95-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="d2a95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2a95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a95-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="d2a95-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2a95-109">*лпсубкэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-110">Имя раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="d2a95-110">The name of the registry key.</span></span> <span data-ttu-id="d2a95-111">Этот ключ должен быть подразделом ключа, указанного параметром *Handle* .</span><span class="sxs-lookup"><span data-stu-id="d2a95-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="d2a95-112">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2a95-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="d2a95-113">Имена ключей не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="d2a95-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="d2a95-114">*лпвалуе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-115">Имя значения реестра.</span><span class="sxs-lookup"><span data-stu-id="d2a95-115">The name of the registry value.</span></span> <span data-ttu-id="d2a95-116">Если этот параметр имеет **значение NULL** или является пустой строкой, функция получает тип и данные для безымянного ключа или значения по умолчанию, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="d2a95-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="d2a95-117">Дополнительные сведения см. в разделе [ограничения размера элементов реестра](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="d2a95-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="d2a95-118">Ключи не имеют автоматически неименованное или значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2a95-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="d2a95-119">Безымянные значения могут быть любого типа.</span><span class="sxs-lookup"><span data-stu-id="d2a95-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="d2a95-120">В именах значений регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="d2a95-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="d2a95-121">*пдвтипе* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-122">Указатель на переменную, которая получает код, указывающий тип данных, хранящихся в указанном значении.</span><span class="sxs-lookup"><span data-stu-id="d2a95-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="d2a95-123">Список возможных кодов типов см. в разделе [типы значений реестра](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="d2a95-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="d2a95-124">Если тип не является обязательным, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="d2a95-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="d2a95-125">*пвдата* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-126">Указатель на буфер, который получает данные значения.</span><span class="sxs-lookup"><span data-stu-id="d2a95-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="d2a95-127">Если данные не требуются, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="d2a95-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="d2a95-128">Если данные являются строкой, функция проверяет наличие завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="d2a95-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="d2a95-129">Если он не найден, строка сохраняется с нулевым символом конца, если буфер достаточно велик для размещения дополнительного символа.</span><span class="sxs-lookup"><span data-stu-id="d2a95-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="d2a95-130">В противном случае функция завершается с ошибкой и возвращает \_ Дополнительные \_ данные.</span><span class="sxs-lookup"><span data-stu-id="d2a95-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="d2a95-131">*пкбдата* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a95-132">Указатель на переменную, указывающую размер буфера, на который указывает параметр *пвдата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="d2a95-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="d2a95-133">При возврате функции эта переменная содержит размер данных, копируемых в *пвдата*.</span><span class="sxs-lookup"><span data-stu-id="d2a95-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="d2a95-134">Параметр *пкбдата* может иметь **значение NULL** , только если *пвдата* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2a95-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="d2a95-135">Если данные имеют \_ тип SZ, REG \_ Multi \_ SZ или REG \_ expand \_ SZ, этот размер включает в себя любой завершающий нуль символ или символы.</span><span class="sxs-lookup"><span data-stu-id="d2a95-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="d2a95-136">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d2a95-136">For more information, see Remarks.</span></span>

<span data-ttu-id="d2a95-137">Если буфер, указанный параметром *пвдата* , недостаточно велик для хранения данных, функция возвращает ошибку \_ больше \_ данных и сохраняет требуемый размер буфера в переменной, на которую указывает *пкбдата*.</span><span class="sxs-lookup"><span data-stu-id="d2a95-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="d2a95-138">В этом случае содержимое буфера *пвдата* не определено.</span><span class="sxs-lookup"><span data-stu-id="d2a95-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="d2a95-139">Если *пвдата* имеет **значение NULL**, а *пкбдата* не имеет **значение NULL**, функция возвращает ошибку \_ Success и сохраняет размер данных в байтах в переменной, на которую указывает *пкбдата*.</span><span class="sxs-lookup"><span data-stu-id="d2a95-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="d2a95-140">Это позволяет приложению определить лучший способ выделения буфера для данных значения.</span><span class="sxs-lookup"><span data-stu-id="d2a95-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a95-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2a95-141">Return value</span></span>

<span data-ttu-id="d2a95-142">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d2a95-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d2a95-143">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d2a95-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="d2a95-144">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="d2a95-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a95-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2a95-145">Remarks</span></span>

<span data-ttu-id="d2a95-146">Приложение обычно вызывает функцию [**оренумвалуе**](orenumvalue.md) для определения имен значений, а затем вызывает функцию **оржетвалуе** для получения данных для имен.</span><span class="sxs-lookup"><span data-stu-id="d2a95-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a95-147">Требования</span><span class="sxs-lookup"><span data-stu-id="d2a95-147">Requirements</span></span>



| <span data-ttu-id="d2a95-148">Требование</span><span class="sxs-lookup"><span data-stu-id="d2a95-148">Requirement</span></span> | <span data-ttu-id="d2a95-149">Значение</span><span class="sxs-lookup"><span data-stu-id="d2a95-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a95-150">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d2a95-150">Redistributable</span></span><br/> | <span data-ttu-id="d2a95-151">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d2a95-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="d2a95-152">Header</span><span class="sxs-lookup"><span data-stu-id="d2a95-152">Header</span></span><br/>          | <dl> <span data-ttu-id="d2a95-153"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a95-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2a95-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a95-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="d2a95-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a95-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a95-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2a95-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a95-157">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="d2a95-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="d2a95-158">**оренумкэй**</span><span class="sxs-lookup"><span data-stu-id="d2a95-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="d2a95-159">**оренумвалуе**</span><span class="sxs-lookup"><span data-stu-id="d2a95-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="d2a95-160">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="d2a95-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="d2a95-161">**оркуеринфокэй**</span><span class="sxs-lookup"><span data-stu-id="d2a95-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
