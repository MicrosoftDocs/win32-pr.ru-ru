---
description: Расшифровывает пакет с одним протоколом SSL (SSL).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Функция Сслдекриптпаккет (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991616"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="dbf88-103">Функция Сслдекриптпаккет</span><span class="sxs-lookup"><span data-stu-id="dbf88-103">SslDecryptPacket function</span></span>

<span data-ttu-id="dbf88-104">Функция **сслдекриптпаккет** SSL расшифровывает пакет [*протокола*](/windows/desktop/SecGloss/s-gly) SSL.</span><span class="sxs-lookup"><span data-stu-id="dbf88-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbf88-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dbf88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbf88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf88-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="dbf88-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-109">*hKey* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-110">Маркер ключа, используемый для расшифровки пакета.</span><span class="sxs-lookup"><span data-stu-id="dbf88-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-111">*пбинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-112">Указатель на буфер, содержащий пакет для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="dbf88-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-113">*кбинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-114">Длина буфера *пбинпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="dbf88-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-115">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-116">Указатель на буфер, в котором будет содержаться расшифрованный пакет.</span><span class="sxs-lookup"><span data-stu-id="dbf88-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-117">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-118">Длина (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="dbf88-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-119">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-120">Число байтов, записанных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="dbf88-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-121">*SequenceNumber* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-122">Порядковый номер, соответствующий этому пакету.</span><span class="sxs-lookup"><span data-stu-id="dbf88-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="dbf88-123">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf88-124">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="dbf88-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf88-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbf88-125">Return value</span></span>

<span data-ttu-id="dbf88-126">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="dbf88-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dbf88-127">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dbf88-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dbf88-128">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="dbf88-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dbf88-129">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="dbf88-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="dbf88-130">Описание</span><span class="sxs-lookup"><span data-stu-id="dbf88-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="dbf88-131">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dbf88-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="dbf88-132">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="dbf88-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbf88-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf88-133">Remarks</span></span>

<span data-ttu-id="dbf88-134">Длина пакета может быть равна нулю, например при расшифровке сообщения "Хеллорекуест".</span><span class="sxs-lookup"><span data-stu-id="dbf88-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf88-135">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf88-135">Requirements</span></span>



| <span data-ttu-id="dbf88-136">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf88-136">Requirement</span></span> | <span data-ttu-id="dbf88-137">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf88-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf88-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbf88-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf88-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dbf88-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbf88-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf88-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbf88-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dbf88-142">Header</span><span class="sxs-lookup"><span data-stu-id="dbf88-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf88-143"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf88-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dbf88-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf88-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf88-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf88-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

