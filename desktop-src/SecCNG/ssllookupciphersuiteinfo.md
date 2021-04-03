---
description: Извлекает сведения о наборе шифров для указанного протокола, набора шифров и набора типов ключей.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Функция СсллукупЦиферсуитеинфо (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913635"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="81e82-103">Функция СсллукупЦиферсуитеинфо</span><span class="sxs-lookup"><span data-stu-id="81e82-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="81e82-104">Функция **ссллукупЦиферсуитеинфо** извлекает сведения о наборе шифров для указанного протокола, набора шифров и набора типов ключей.</span><span class="sxs-lookup"><span data-stu-id="81e82-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81e82-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="81e82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81e82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e82-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81e82-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-108">Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="81e82-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="81e82-109">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81e82-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-110">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="81e82-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="81e82-111">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81e82-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-112">Один из значений [**идентификаторов комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="81e82-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="81e82-113">*двкэйтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81e82-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-114">Одно из значений [**идентификаторов типа ключа поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="81e82-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="81e82-115">*пЦиферсуите* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81e82-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-116">Адрес буфера, содержащего структуру [**\_ \_ \_ набора шифров NCRYPT SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) , в которую записываются сведения о наборе шифров.</span><span class="sxs-lookup"><span data-stu-id="81e82-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="81e82-117">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81e82-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e82-118">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="81e82-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e82-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81e82-119">Return value</span></span>

<span data-ttu-id="81e82-120">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="81e82-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="81e82-121">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="81e82-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="81e82-122">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="81e82-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="81e82-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="81e82-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="81e82-124">Описание</span><span class="sxs-lookup"><span data-stu-id="81e82-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="81e82-125">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="81e82-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="81e82-126">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="81e82-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81e82-127">Требования</span><span class="sxs-lookup"><span data-stu-id="81e82-127">Requirements</span></span>



| <span data-ttu-id="81e82-128">Требование</span><span class="sxs-lookup"><span data-stu-id="81e82-128">Requirement</span></span> | <span data-ttu-id="81e82-129">Значение</span><span class="sxs-lookup"><span data-stu-id="81e82-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e82-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81e82-130">Minimum supported client</span></span><br/> | <span data-ttu-id="81e82-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81e82-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="81e82-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81e82-132">Minimum supported server</span></span><br/> | <span data-ttu-id="81e82-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81e82-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="81e82-134">Header</span><span class="sxs-lookup"><span data-stu-id="81e82-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e82-135"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e82-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="81e82-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81e82-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e82-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e82-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

