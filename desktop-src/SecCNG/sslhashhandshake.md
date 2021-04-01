---
description: Возвращает маркер для хеша подтверждения.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Функция Сслхашхандшаке (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999229"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="287ec-103">Функция Сслхашхандшаке</span><span class="sxs-lookup"><span data-stu-id="287ec-103">SslHashHandshake function</span></span>

<span data-ttu-id="287ec-104">Функция **сслхашхандшаке** возвращает маркер для хеша подтверждения.</span><span class="sxs-lookup"><span data-stu-id="287ec-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="287ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="287ec-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="287ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="287ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="287ec-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="287ec-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="287ec-108">Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="287ec-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="287ec-109">*ххандшакехаш* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="287ec-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="287ec-110">Маркер для хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="287ec-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="287ec-111">*пбинпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="287ec-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="287ec-112">Адрес буфера, содержащего данные для хэширования.</span><span class="sxs-lookup"><span data-stu-id="287ec-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="287ec-113">*кбинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="287ec-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="287ec-114">Размер (в байтах) буфера *пбинпут* .</span><span class="sxs-lookup"><span data-stu-id="287ec-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="287ec-115">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="287ec-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="287ec-116">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="287ec-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="287ec-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="287ec-117">Return value</span></span>

<span data-ttu-id="287ec-118">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="287ec-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="287ec-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="287ec-119">Remarks</span></span>

<span data-ttu-id="287ec-120">Функция **сслхашхандшаке** является одной из трех функций, используемых для создания хэша, используемого во время подтверждения SSL.</span><span class="sxs-lookup"><span data-stu-id="287ec-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="287ec-121">Для получения обработчика хэша вызывается функция [**сслкреатехандшакехаш**](sslcreatehandshakehash.md) .</span><span class="sxs-lookup"><span data-stu-id="287ec-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="287ec-122">Функция **сслхашхандшаке** вызывается любое количество раз с обработчиком хэша для добавления данных в хэш.</span><span class="sxs-lookup"><span data-stu-id="287ec-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="287ec-123">Функция [**сслкомпутефинишедхаш**](sslcomputefinishedhash.md) вызывается с хэш-маркером для получения дайджеста хэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="287ec-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="287ec-124">Требования</span><span class="sxs-lookup"><span data-stu-id="287ec-124">Requirements</span></span>



| <span data-ttu-id="287ec-125">Требование</span><span class="sxs-lookup"><span data-stu-id="287ec-125">Requirement</span></span> | <span data-ttu-id="287ec-126">Значение</span><span class="sxs-lookup"><span data-stu-id="287ec-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="287ec-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="287ec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="287ec-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="287ec-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="287ec-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="287ec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="287ec-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="287ec-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="287ec-131">Header</span><span class="sxs-lookup"><span data-stu-id="287ec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="287ec-132"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="287ec-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="287ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="287ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="287ec-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="287ec-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

