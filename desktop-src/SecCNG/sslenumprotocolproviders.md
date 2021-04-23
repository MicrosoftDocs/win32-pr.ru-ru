---
description: Возвращает массив поставщиков протоколов, SSL установленных по протоколу SSL.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Функция Ссленумпротоколпровидерс (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272769"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="4ff9a-103">Функция Ссленумпротоколпровидерс</span><span class="sxs-lookup"><span data-stu-id="4ff9a-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="4ff9a-104">Функция **ссленумпротоколпровидерс** возвращает массив [*SSL*](/windows/desktop/SecGloss/s-gly) установленных поставщиков протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ff9a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4ff9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ff9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff9a-107">*пдвпровидеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ff9a-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff9a-108">Указатель на значение **DWORD** для получения числа возвращаемых поставщиков протоколов.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="4ff9a-109">*пппровидерлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ff9a-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff9a-110">Указатель на буфер, который получает массив структур [**нкриптпровидернаме**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .</span><span class="sxs-lookup"><span data-stu-id="4ff9a-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="4ff9a-111">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ff9a-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff9a-112">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff9a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ff9a-113">Return value</span></span>

<span data-ttu-id="4ff9a-114">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="4ff9a-115">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="4ff9a-116">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="4ff9a-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4ff9a-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="4ff9a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4ff9a-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4ff9a-119">Не <dt>**превышать \_ Неправильные \_ Флаги**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="4ff9a-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="4ff9a-120">Параметр *dwFlags* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="4ff9a-121">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="4ff9a-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="4ff9a-122">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="4ff9a-123">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="4ff9a-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="4ff9a-124">Параметр *пдвпровидеркаунт* или *Пппровидерлист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ff9a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ff9a-125">Remarks</span></span>

<span data-ttu-id="4ff9a-126">После завершения использования массива структур [**нкриптпровидернаме**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) вызовите функцию [**сслфрибуффер**](sslfreebuffer.md) , чтобы освободить массив.</span><span class="sxs-lookup"><span data-stu-id="4ff9a-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff9a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4ff9a-127">Requirements</span></span>



| <span data-ttu-id="4ff9a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4ff9a-128">Requirement</span></span> | <span data-ttu-id="4ff9a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4ff9a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff9a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ff9a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff9a-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ff9a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ff9a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ff9a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff9a-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ff9a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ff9a-134">Header</span><span class="sxs-lookup"><span data-stu-id="4ff9a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ff9a-135"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff9a-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="4ff9a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4ff9a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ff9a-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ff9a-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

