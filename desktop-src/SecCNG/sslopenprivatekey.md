---
description: Открывает маркер закрытого ключа.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Функция Сслопенприватекэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144482"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="a1831-103">Функция Сслопенприватекэй</span><span class="sxs-lookup"><span data-stu-id="a1831-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="a1831-104">Функция **сслопенприватекэй** открывает маркер [*закрытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="a1831-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1831-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1831-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a1831-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1831-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1831-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-108">Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="a1831-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-109">*фприватекэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a1831-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-110">Адрес буфера, в который записывается маркер для закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="a1831-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="a1831-111">После завершения использования ключа следует освободить *фприватекэй* , вызвав функцию [**сслфриобжект**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a1831-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-112">*пцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1831-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-113">Адрес сертификата, из которого получается закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="a1831-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-114">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1831-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-115">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="a1831-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1831-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1831-116">Return value</span></span>

<span data-ttu-id="a1831-117">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a1831-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a1831-118">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a1831-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a1831-119">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="a1831-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a1831-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a1831-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="a1831-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a1831-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1831-122">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="a1831-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="a1831-123">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="a1831-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="a1831-124">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a1831-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="a1831-125">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="a1831-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="a1831-126">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="a1831-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="a1831-127">Параметр *фприватекэй* или *Пцертконтекст* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a1831-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="a1831-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1831-128">Remarks</span></span>

<span data-ttu-id="a1831-129">Полученный закрытый ключ является частью пары из [*открытого и закрытого ключей*](/windows/desktop/SecGloss/p-gly) в [*сертификате*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="a1831-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="a1831-130">Эта функция просто извлекает закрытый ключ из сертификата, указанного параметром *пцертконтекст* .</span><span class="sxs-lookup"><span data-stu-id="a1831-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1831-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a1831-131">Requirements</span></span>



| <span data-ttu-id="a1831-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a1831-132">Requirement</span></span> | <span data-ttu-id="a1831-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a1831-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1831-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1831-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a1831-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1831-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a1831-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1831-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a1831-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1831-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1831-138">Header</span><span class="sxs-lookup"><span data-stu-id="a1831-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1831-139"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1831-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a1831-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a1831-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1831-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1831-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

