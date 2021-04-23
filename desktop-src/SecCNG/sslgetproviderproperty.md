---
description: Извлекает значение указанного свойства поставщика.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Функция Сслжетпровидерпроперти (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912284"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="fb32a-103">Функция Сслжетпровидерпроперти</span><span class="sxs-lookup"><span data-stu-id="fb32a-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="fb32a-104">Функция **сслжетпровидерпроперти** извлекает значение указанного свойства поставщика.</span><span class="sxs-lookup"><span data-stu-id="fb32a-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb32a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb32a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fb32a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb32a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb32a-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-108">Маркер поставщика [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL), для которого извлекается свойство.</span><span class="sxs-lookup"><span data-stu-id="fb32a-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="fb32a-109">*псзпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-110">Указатель на строку в Юникоде, завершающуюся нулем, которая содержит имя извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="fb32a-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="fb32a-111">*ппбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-112">Адрес буфера, который получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fb32a-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="fb32a-113">Вызывающая функция должна освободить этот буфер, вызвав функцию [**сслфрибуффер**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fb32a-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fb32a-114">*пкбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-115">Размер (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="fb32a-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fb32a-116">*ппенумстате* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-117">Адрес указателя **void** , который получает сведения о состоянии перечисления, используемые в последующих вызовах этой функции.</span><span class="sxs-lookup"><span data-stu-id="fb32a-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="fb32a-118">Эта информация имеет значение только для поставщика SSL и непрозрачна для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="fb32a-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="fb32a-119">Поставщик SSL использует эти сведения для определения того, какой элемент находится далее в перечислении.</span><span class="sxs-lookup"><span data-stu-id="fb32a-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="fb32a-120">Если переменная, на которую указывает этот параметр, содержит **значение NULL**, перечисление запускается с самого начала.</span><span class="sxs-lookup"><span data-stu-id="fb32a-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="fb32a-121">Вызывающая функция должна освободить эту память путем вызова функции [**сслфрибуффер**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fb32a-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fb32a-122">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb32a-123">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="fb32a-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb32a-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb32a-124">Return value</span></span>

<span data-ttu-id="fb32a-125">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fb32a-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="fb32a-126">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb32a-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="fb32a-127">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="fb32a-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fb32a-128">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="fb32a-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="fb32a-129">Описание</span><span class="sxs-lookup"><span data-stu-id="fb32a-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb32a-130">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="fb32a-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="fb32a-131">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="fb32a-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="fb32a-132">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fb32a-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="fb32a-133">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="fb32a-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="fb32a-134">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="fb32a-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="fb32a-135">Один из переданных параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="fb32a-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="fb32a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="fb32a-136">Requirements</span></span>



| <span data-ttu-id="fb32a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="fb32a-137">Requirement</span></span> | <span data-ttu-id="fb32a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="fb32a-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb32a-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb32a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fb32a-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fb32a-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb32a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fb32a-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb32a-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fb32a-143">Header</span><span class="sxs-lookup"><span data-stu-id="fb32a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb32a-144"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb32a-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fb32a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fb32a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb32a-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb32a-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

