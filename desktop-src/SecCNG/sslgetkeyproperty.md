---
description: Получает значение именованного свойства SSL для объекта ключа поставщика протокола SSL.
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Функция Сслжеткэйпроперти (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664257"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="dfb6f-103">Функция Сслжеткэйпроперти</span><span class="sxs-lookup"><span data-stu-id="dfb6f-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="dfb6f-104">Функция **сслжеткэйпроперти** извлекает значение именованного свойства SSL для объекта ключа поставщика [*протокола*](/windows/desktop/SecGloss/s-gly) SSL.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfb6f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dfb6f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfb6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb6f-107">*hKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb6f-108">Маркер поставщика SSL.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="dfb6f-109">*псзпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb6f-110">Указатель на строку в Юникоде, завершающуюся нулем, которая содержит имя извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="dfb6f-111">Это может быть один из стандартных [**идентификаторов свойств хранилища ключей**](key-storage-property-identifiers.md) или идентификатор настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dfb6f-112">*ппбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb6f-113">Указатель на буфер, который получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="dfb6f-114">Вызывающая функция должна освободить этот буфер, вызвав функцию [**сслфрибуффер**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb6f-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dfb6f-115">*пкбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb6f-116">Размер (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="dfb6f-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dfb6f-117">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb6f-118">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb6f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfb6f-119">Return value</span></span>

<span data-ttu-id="dfb6f-120">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dfb6f-121">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dfb6f-122">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dfb6f-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="dfb6f-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="dfb6f-124">Описание</span><span class="sxs-lookup"><span data-stu-id="dfb6f-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="dfb6f-125">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfb6f-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="dfb6f-126">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="dfb6f-127">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="dfb6f-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="dfb6f-128">Один из переданных параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="dfb6f-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dfb6f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="dfb6f-129">Requirements</span></span>



| <span data-ttu-id="dfb6f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="dfb6f-130">Requirement</span></span> | <span data-ttu-id="dfb6f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="dfb6f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb6f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfb6f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb6f-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dfb6f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfb6f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb6f-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfb6f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dfb6f-136">Header</span><span class="sxs-lookup"><span data-stu-id="dfb6f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb6f-137"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb6f-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dfb6f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb6f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb6f-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb6f-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

