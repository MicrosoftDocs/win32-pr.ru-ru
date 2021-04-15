---
description: Получает виртуальные флаги указанного открытого раздела реестра в автономном кусте реестра.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Функция Оржетвиртуалфлагс (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648833"
---
# <a name="orgetvirtualflags-function"></a><span data-ttu-id="68205-103">Функция Оржетвиртуалфлагс</span><span class="sxs-lookup"><span data-stu-id="68205-103">ORGetVirtualFlags function</span></span>

<span data-ttu-id="68205-104">Получает виртуальные флаги указанного открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="68205-104">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="68205-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68205-105">Syntax</span></span>


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="68205-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68205-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68205-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68205-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68205-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="68205-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="68205-109">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68205-109">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68205-110">Указатель на переменную для получения флагов виртуализации, заданных для ключа.</span><span class="sxs-lookup"><span data-stu-id="68205-110">A pointer to a variable to receive the virtualization flags set for the key.</span></span> <span data-ttu-id="68205-111">После возврата функции этот параметр может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="68205-111">After the function returns, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="68205-112">Значение</span><span class="sxs-lookup"><span data-stu-id="68205-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="68205-113">Значение</span><span class="sxs-lookup"><span data-stu-id="68205-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="68205-114"><dt>**Reg \_ КЛЮЧ \_ не \_ Автоматический \_ сбой**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="68205-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="68205-115">Если этот флаг установлен и операция открытия завершается сбоем для ключа с включенной виртуализацией, реестр не пытается повторно открыть ключ.</span><span class="sxs-lookup"><span data-stu-id="68205-115">If this flag is set and an Open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="68205-116">Если этот флаг снят, реестр пытается повторно открыть раздел с МАКСИМАЛЬным \_ допустимым доступом.</span><span class="sxs-lookup"><span data-stu-id="68205-116">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="68205-117"><dt>**Reg \_ KEY \_ не \_ виртуализация**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="68205-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="68205-118">Если этот флаг установлен и операция создания ключа завершается неудачей, так как вызывающий объект не имеет \_ \_ \_ право на создание подраздела в родительском ключе, реестр завершает операцию создания.</span><span class="sxs-lookup"><span data-stu-id="68205-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="68205-119">Если этот флаг снят, реестр пытается создать ключ в виртуальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="68205-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="68205-120">Вызывающий объект должен иметь ключ \_ Read Right для родительского ключа.</span><span class="sxs-lookup"><span data-stu-id="68205-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="68205-121"><dt>**Reg \_ \_ \_ Флаг рекурсии ключа**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="68205-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="68205-122">Если этот флаг установлен, флаги виртуализации реестра распространяются из родительского ключа.</span><span class="sxs-lookup"><span data-stu-id="68205-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="68205-123">Если этот флаг снят, флаги виртуализации реестра не распространяются.</span><span class="sxs-lookup"><span data-stu-id="68205-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68205-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68205-124">Return value</span></span>

<span data-ttu-id="68205-125">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="68205-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="68205-126">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="68205-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="68205-127">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="68205-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="68205-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68205-128">Remarks</span></span>

<span data-ttu-id="68205-129">Виртуализация реестра — это промежуточная технология обеспечения совместимости приложений, которая позволяет выполнять операции записи в реестре, которые имеют глобальное влияние на расположение пользователей.</span><span class="sxs-lookup"><span data-stu-id="68205-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="68205-130">Это перенаправление прозрачно для приложений, читающих или записывающих в реестр.</span><span class="sxs-lookup"><span data-stu-id="68205-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="68205-131">Виртуализация реестра поддерживается начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68205-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="68205-132">Тем не менее, корпорация Майкрософт планирует удалить ее из будущих версий операционной системы Windows по мере того, как другие приложения становятся совместимыми с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68205-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="68205-133">Поэтому приложения не должны зависеть от поведения виртуализации реестра в системе.</span><span class="sxs-lookup"><span data-stu-id="68205-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="68205-134">Виртуализация реестра включена только в следующих целях:</span><span class="sxs-lookup"><span data-stu-id="68205-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="68205-135">32-разрядные интерактивные процессы</span><span class="sxs-lookup"><span data-stu-id="68205-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="68205-136">Ключи в **\_ \_ \\ программном обеспечении для локального компьютера hKey**</span><span class="sxs-lookup"><span data-stu-id="68205-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="68205-137">Ключи, в которые администратор может выполнять запись</span><span class="sxs-lookup"><span data-stu-id="68205-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="68205-138">Дополнительные сведения см. в разделе [Виртуализация реестра](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="68205-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68205-139">Требования</span><span class="sxs-lookup"><span data-stu-id="68205-139">Requirements</span></span>



| <span data-ttu-id="68205-140">Требование</span><span class="sxs-lookup"><span data-stu-id="68205-140">Requirement</span></span> | <span data-ttu-id="68205-141">Значение</span><span class="sxs-lookup"><span data-stu-id="68205-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68205-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="68205-142">Redistributable</span></span><br/> | <span data-ttu-id="68205-143">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="68205-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="68205-144">Header</span><span class="sxs-lookup"><span data-stu-id="68205-144">Header</span></span><br/>          | <dl> <span data-ttu-id="68205-145"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="68205-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="68205-146">DLL</span><span class="sxs-lookup"><span data-stu-id="68205-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="68205-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68205-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68205-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68205-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68205-149">**орсетвиртуалфлагс**</span><span class="sxs-lookup"><span data-stu-id="68205-149">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="68205-150">Виртуализация реестра</span><span class="sxs-lookup"><span data-stu-id="68205-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
