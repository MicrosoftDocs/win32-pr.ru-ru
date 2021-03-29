---
description: Создает эфемерный ключ для использования во время проверки подлинности, которая происходит SSL при подтверждении протокола SSL.
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Функция Сслкреатифемералкэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647295"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="3624e-103">Функция Сслкреатифемералкэй</span><span class="sxs-lookup"><span data-stu-id="3624e-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="3624e-104">Функция **сслкреатифемералкэй** создает эфемерный ключ для использования во время проверки подлинности, которая происходит [*SSL*](/windows/desktop/SecGloss/s-gly) при подтверждении протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="3624e-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="3624e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3624e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3624e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3624e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3624e-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="3624e-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-109">*фефемералкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3624e-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-110">Маркер эфемерного ключа.</span><span class="sxs-lookup"><span data-stu-id="3624e-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-111">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-112">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="3624e-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-113">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-114">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="3624e-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-115">*двкэйтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-116">Одно из значений [**идентификатора типа ключа поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="3624e-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="3624e-117">Присвойте этому параметру нулевое значение для типов ключей, которые не поддерживают шифрование на основе [*эллиптических*](/windows/desktop/SecGloss/e-gly) кривых (ECC).</span><span class="sxs-lookup"><span data-stu-id="3624e-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="3624e-118">*двкэйбитлен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-119">Длина ключа в битах.</span><span class="sxs-lookup"><span data-stu-id="3624e-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-120">*пбпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-121">Указатель на буфер, содержащий параметры для создаваемого ключа.</span><span class="sxs-lookup"><span data-stu-id="3624e-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="3624e-122">Если набор шифров для [*алгоритма Диффи-Хелмана (*](/windows/desktop/SecGloss/d-gly) дхе) не используется, присвойте параметру *пбпарамс* **значение NULL** , а параметр *кбпарамс* — нулю.</span><span class="sxs-lookup"><span data-stu-id="3624e-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-123">*кбпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-124">Длина (в байтах) данных в буфере *пбпарамс* .</span><span class="sxs-lookup"><span data-stu-id="3624e-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3624e-125">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3624e-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3624e-126">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="3624e-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3624e-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3624e-127">Return value</span></span>

<span data-ttu-id="3624e-128">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3624e-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3624e-129">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="3624e-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="3624e-130">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3624e-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="3624e-131">Описание</span><span class="sxs-lookup"><span data-stu-id="3624e-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3624e-132">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="3624e-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="3624e-133">Недостаточно памяти для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="3624e-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="3624e-134">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3624e-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="3624e-135">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="3624e-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="3624e-136">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="3624e-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="3624e-137">Один из переданных параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="3624e-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="3624e-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3624e-138">Remarks</span></span>

<span data-ttu-id="3624e-139">При использовании набора шифров ДХЕ внутренняя реализация SSL передает параметры сервера *p* и *g* в функцию **сслкреатифемералкэй** в параметрах *пбпарамс* и *кбпарамс* .</span><span class="sxs-lookup"><span data-stu-id="3624e-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="3624e-140">Формат данных в буфере *пбпарамс* тот же, который использовался при задании свойства [**\_ \_ параметров BCrypt DH**](cng-property-identifiers.md) , и начинается с структуры [**\_ \_ \_ заголовка параметра BCrypt DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="3624e-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3624e-141">Требования</span><span class="sxs-lookup"><span data-stu-id="3624e-141">Requirements</span></span>



| <span data-ttu-id="3624e-142">Требование</span><span class="sxs-lookup"><span data-stu-id="3624e-142">Requirement</span></span> | <span data-ttu-id="3624e-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3624e-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3624e-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3624e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3624e-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3624e-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3624e-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3624e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3624e-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3624e-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3624e-148">Header</span><span class="sxs-lookup"><span data-stu-id="3624e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3624e-149"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="3624e-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3624e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3624e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3624e-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3624e-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

