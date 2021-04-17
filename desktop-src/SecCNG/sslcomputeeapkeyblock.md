---
description: Вычисление блока ключей, используемого протоколом EAP.
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Функция Сслкомпутиапкэйблокк (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662867"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="3ad7b-103">Функция Сслкомпутиапкэйблокк</span><span class="sxs-lookup"><span data-stu-id="3ad7b-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="3ad7b-104">Функция **сслкомпутиапкэйблокк** вычислит блок ключей, используемый протоколом EAP.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad7b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ad7b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3ad7b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ad7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad7b-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="3ad7b-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-109">*хмастеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-110">Маркер объекта [*главного ключа*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="3ad7b-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-111">*пбрандомс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-112">Указатель на буфер, который содержит сцепление \_ случайных и серверных \_ случайных значений сеанса SSL.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-113">*кбрандомс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-114">Длина буфера *пбрандомс* в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-115">*пбаутпут* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-116">Адрес буфера, который получает большой двоичный объект ключа.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="3ad7b-117">Параметр *кбаутпут* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="3ad7b-118">Если этот параметр имеет **значение NULL**, эта функция поместит требуемый размер (в байтах) в **DWORD** , на который указывает параметр *пкбресулт* .</span><span class="sxs-lookup"><span data-stu-id="3ad7b-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-119">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-120">Длина буфера *пбаутпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-121">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-122">Указатель на значение **DWORD** , определяющее длину хэша в байтах, записанных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="3ad7b-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7b-123">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad7b-124">Установите **флаг NCRYPT \_ SSL \_ - \_ сервера** , чтобы указать, что это вызов сервера.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad7b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ad7b-125">Return value</span></span>

<span data-ttu-id="3ad7b-126">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3ad7b-127">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="3ad7b-128">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3ad7b-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3ad7b-129">Описание</span><span class="sxs-lookup"><span data-stu-id="3ad7b-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3ad7b-130">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ad7b-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="3ad7b-131">Один из представленных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="3ad7b-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ad7b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3ad7b-132">Requirements</span></span>



| <span data-ttu-id="3ad7b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3ad7b-133">Requirement</span></span> | <span data-ttu-id="3ad7b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3ad7b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad7b-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ad7b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad7b-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ad7b-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ad7b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad7b-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ad7b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ad7b-139">Header</span><span class="sxs-lookup"><span data-stu-id="3ad7b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad7b-140"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad7b-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3ad7b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3ad7b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad7b-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ad7b-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

