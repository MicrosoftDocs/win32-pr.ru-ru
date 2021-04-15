---
description: Шифрует пакет с одним протоколом SSL (SSL).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Функция Ссленкриптпаккет (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647725"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="87f9f-103">Функция Ссленкриптпаккет</span><span class="sxs-lookup"><span data-stu-id="87f9f-103">SslEncryptPacket function</span></span>

<span data-ttu-id="87f9f-104">Функция **ссленкриптпаккет** шифрует пакет с одним [*протоколом SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="87f9f-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f9f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="87f9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f9f-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="87f9f-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-109">*hKey* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-110">Маркер ключа, используемый для шифрования пакета.</span><span class="sxs-lookup"><span data-stu-id="87f9f-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-111">*пбинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-112">Указатель на буфер, содержащий пакет для шифрования.</span><span class="sxs-lookup"><span data-stu-id="87f9f-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-113">*кбинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-114">Длина буфера *пбинпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="87f9f-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-115">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-116">Указатель на буфер для получения зашифрованного пакета.</span><span class="sxs-lookup"><span data-stu-id="87f9f-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-117">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-118">Длина (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="87f9f-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-119">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-120">Число байтов, записанных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="87f9f-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-121">*SequenceNumber* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-122">Порядковый номер, соответствующий этому пакету.</span><span class="sxs-lookup"><span data-stu-id="87f9f-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="87f9f-123">*двконтенттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-124">Тип содержимого, соответствующий этому пакету, который указывает протокол более высокого уровня, используемый для обработки заключенного в пакет пакета.</span><span class="sxs-lookup"><span data-stu-id="87f9f-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="87f9f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="87f9f-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="87f9f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="87f9f-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="87f9f-127"><dt>**CT \_ ИЗМЕНЕНИЕ \_ шифра, \_ Спецификация**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="87f9f-128">Указывает на изменение в стратегии шифра.</span><span class="sxs-lookup"><span data-stu-id="87f9f-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="87f9f-129"><dt>**CT \_ ПРЕДУПРЕЖДЕНИЕ**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="87f9f-130">Указывает, что вложенный пакет содержит предупреждение.</span><span class="sxs-lookup"><span data-stu-id="87f9f-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="87f9f-131"><dt>**CT \_ ПОДТВЕРЖДЕНИЕ**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="87f9f-132">Указывает, что вложенный пакет является частью протокола подтверждения.</span><span class="sxs-lookup"><span data-stu-id="87f9f-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="87f9f-133"><dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="87f9f-134">Указывает, что пакет содержит данные приложения.</span><span class="sxs-lookup"><span data-stu-id="87f9f-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="87f9f-135">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f9f-136">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="87f9f-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f9f-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87f9f-137">Return value</span></span>

<span data-ttu-id="87f9f-138">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="87f9f-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="87f9f-139">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="87f9f-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="87f9f-140">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="87f9f-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="87f9f-141">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="87f9f-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="87f9f-142">Описание</span><span class="sxs-lookup"><span data-stu-id="87f9f-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="87f9f-143">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="87f9f-144">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="87f9f-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87f9f-145">Требования</span><span class="sxs-lookup"><span data-stu-id="87f9f-145">Requirements</span></span>



| <span data-ttu-id="87f9f-146">Требование</span><span class="sxs-lookup"><span data-stu-id="87f9f-146">Requirement</span></span> | <span data-ttu-id="87f9f-147">Значение</span><span class="sxs-lookup"><span data-stu-id="87f9f-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f9f-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87f9f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="87f9f-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87f9f-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87f9f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="87f9f-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87f9f-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87f9f-152">Header</span><span class="sxs-lookup"><span data-stu-id="87f9f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f9f-153"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="87f9f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="87f9f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f9f-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87f9f-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

