---
description: Открывает указанный раздел реестра в автономном кусте реестра.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Функция Оропенкэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648951"
---
# <a name="oropenkey-function"></a><span data-ttu-id="78d8f-103">Функция Оропенкэй</span><span class="sxs-lookup"><span data-stu-id="78d8f-103">OROpenKey function</span></span>

<span data-ttu-id="78d8f-104">Открывает указанный раздел реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="78d8f-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d8f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78d8f-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="78d8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78d8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d8f-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78d8f-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d8f-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="78d8f-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="78d8f-109">*лпсубкэйнаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="78d8f-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78d8f-110">Указатель на строку в Юникоде, содержащую имя открываемого раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="78d8f-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="78d8f-111">Этот ключ должен быть подразделом ключа, определяемого параметром *Handle* .</span><span class="sxs-lookup"><span data-stu-id="78d8f-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="78d8f-112">Имена ключей не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="78d8f-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="78d8f-113">Если этот параметр имеет **значение NULL** или указатель на пустую строку, функция возвращает тот же переданный обработчик.</span><span class="sxs-lookup"><span data-stu-id="78d8f-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="78d8f-114">Если ключ, заданный параметром *Handle* , является корневым ключом Hive, функция возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="78d8f-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="78d8f-115">Дополнительные сведения см. в разделе [ограничения размера элементов реестра](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="78d8f-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="78d8f-116">*фкресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78d8f-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d8f-117">Указатель на переменную, которая получает маркер открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="78d8f-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="78d8f-118">Используйте функцию [**орклосекэй**](orclosekey.md) , чтобы закрыть ключ после завершения использования маркера.</span><span class="sxs-lookup"><span data-stu-id="78d8f-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d8f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78d8f-119">Return value</span></span>

<span data-ttu-id="78d8f-120">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="78d8f-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="78d8f-121">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="78d8f-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="78d8f-122">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="78d8f-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="78d8f-123">Если возвращаемый маркер будет маркером корневого ключа Hive, функция возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="78d8f-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="78d8f-124">Если указанный ключ был помечен как удаленный, эта функция возвращает \_ ключ ошибки \_ deleted.</span><span class="sxs-lookup"><span data-stu-id="78d8f-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d8f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78d8f-125">Remarks</span></span>

<span data-ttu-id="78d8f-126">Функцию **оропенкэй** нельзя использовать для открытия корневого ключа в кусте реестра вне сети.</span><span class="sxs-lookup"><span data-stu-id="78d8f-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="78d8f-127">Чтобы получить маркер корневого ключа Hive, используйте функцию [**оропенхиве**](oropenhive.md) для загрузки Hive в память.</span><span class="sxs-lookup"><span data-stu-id="78d8f-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d8f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="78d8f-128">Requirements</span></span>



| <span data-ttu-id="78d8f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="78d8f-129">Requirement</span></span> | <span data-ttu-id="78d8f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="78d8f-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78d8f-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="78d8f-131">Redistributable</span></span><br/> | <span data-ttu-id="78d8f-132">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="78d8f-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="78d8f-133">Header</span><span class="sxs-lookup"><span data-stu-id="78d8f-133">Header</span></span><br/>          | <dl> <span data-ttu-id="78d8f-134"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d8f-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="78d8f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="78d8f-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="78d8f-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78d8f-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d8f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78d8f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d8f-138">**орклосекэй**</span><span class="sxs-lookup"><span data-stu-id="78d8f-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="78d8f-139">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="78d8f-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="78d8f-140">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="78d8f-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="78d8f-141">**оропенхиве**</span><span class="sxs-lookup"><span data-stu-id="78d8f-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
