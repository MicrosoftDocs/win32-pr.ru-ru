---
description: Расшифровывает сообщение с помощью NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Функция Декриптмессаже (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719556"
---
# <a name="decryptmessage-ntlm-function"></a><span data-ttu-id="cbe93-103">Функция Декриптмессаже (NTLM)</span><span class="sxs-lookup"><span data-stu-id="cbe93-103">DecryptMessage (NTLM) function</span></span>

<span data-ttu-id="cbe93-104">Функция **декриптмессаже (NTLM)** расшифровывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="cbe93-104">The **DecryptMessage (NTLM)** function decrypts a message.</span></span> <span data-ttu-id="cbe93-105">Некоторые пакеты не шифруют и не расшифровываются сообщения, а выполняют и проверяют [*хэш*](../secgloss/h-gly.md)целостности.</span><span class="sxs-lookup"><span data-stu-id="cbe93-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="cbe93-106">[**Енкриптмессаже (NTLM)**](encryptmessage--ntlm.md) и **декриптмессаже (NTLM)** могут вызываться одновременно из двух разных потоков в одном контексте SSPI, если [*один поток*](../secgloss/s-gly.md) шифруется, а другой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="cbe93-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) and **DecryptMessage (NTLM)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="cbe93-107">При шифровании нескольких потоков или при расшифровке более одного потока каждый поток должен получить уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="cbe93-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe93-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbe93-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="cbe93-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbe93-109">Parameters</span></span>

<span data-ttu-id="cbe93-110">*фконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-110">*phContext* \[in\]</span></span>

<span data-ttu-id="cbe93-111">Маркер [*контекста безопасности*](../secgloss/s-gly.md) , который будет использоваться для расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbe93-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="cbe93-112">*пмессаже* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="cbe93-113">Указатель на структуру [**секбуффердеск**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="cbe93-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="cbe93-114">На входе структура ссылается на одну или несколько структур [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cbe93-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="cbe93-115">По крайней мере один из них должен иметь тип \_ данных pvbuffer.</span><span class="sxs-lookup"><span data-stu-id="cbe93-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="cbe93-116">Этот буфер содержит зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="cbe93-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="cbe93-117">Зашифрованное сообщение расшифровывается на месте, переписывая исходное содержимое его буфера.</span><span class="sxs-lookup"><span data-stu-id="cbe93-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="cbe93-118">*Мессажесекно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="cbe93-119">Порядковый номер, ожидаемый транспортным приложением (при наличии).</span><span class="sxs-lookup"><span data-stu-id="cbe93-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="cbe93-120">Если транспортное приложение не поддерживает порядковые номера, этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="cbe93-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="cbe93-121">*пфкоп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="cbe93-122">Указатель на переменную типа **ulong** , которая получает зависящие от пакета флаги, указывающие качество защиты.</span><span class="sxs-lookup"><span data-stu-id="cbe93-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="cbe93-123">Этот параметр может иметь следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="cbe93-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="cbe93-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe93-124">Value</span></span></th><th><span data-ttu-id="cbe93-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe93-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="cbe93-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cbe93-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="cbe93-127">Сообщение не было зашифровано, но был создан заголовок или трейлер.</span><span class="sxs-lookup"><span data-stu-id="cbe93-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="cbe93-128">KERB_WRAP_NO_ENCRYPT имеет то же значение и то же самое.</span><span class="sxs-lookup"><span data-stu-id="cbe93-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="cbe93-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbe93-129">Return value</span></span>

<span data-ttu-id="cbe93-130">Если функция проверяет, что сообщение было получено в правильной последовательности, функция возвращает значение в секунду \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cbe93-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="cbe93-131">Если функция не расшифрует сообщение, она возвращает один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="cbe93-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="cbe93-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbe93-132">Return code</span></span>                     | <span data-ttu-id="cbe93-133">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe93-133">Description</span></span>                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe93-134">**с \_ \_ неполным \_ сообщением электронной почты**</span><span class="sxs-lookup"><span data-stu-id="cbe93-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="cbe93-135">Данные во входном буфере неполны.</span><span class="sxs-lookup"><span data-stu-id="cbe93-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="cbe93-136">Приложению необходимо прочитать больше данных с сервера и вызвать [**декриптмессаже (NTLM)**](decryptmessage--ntlm.md) еще раз.</span><span class="sxs-lookup"><span data-stu-id="cbe93-136">The application needs to read more data from the server and call [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) again.</span></span> |
| <span data-ttu-id="cbe93-137">**с \_ не \_ \_ по \_ порядку**</span><span class="sxs-lookup"><span data-stu-id="cbe93-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="cbe93-138">Сообщение не было получено в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="cbe93-138">The message was not received in the correct sequence.</span></span>                                                                                                                    |

## <a name="remarks"></a><span data-ttu-id="cbe93-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbe93-139">Remarks</span></span>

<span data-ttu-id="cbe93-140">Иногда приложение будет считывать данные от удаленной стороны, пытаться расшифровать их с помощью **декриптмессаже (NTLM)** и обнаружить, что **декриптмессаже (NTLM)** был удален, но выходные буферы пусты.</span><span class="sxs-lookup"><span data-stu-id="cbe93-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (NTLM)**, and discover that **DecryptMessage (NTLM)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="cbe93-141">Это нормальное поведение, и приложения должны уметь работать с ним.</span><span class="sxs-lookup"><span data-stu-id="cbe93-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="cbe93-142">**Windows XP:** Эта функция также называлась **унсеалмессаже**.</span><span class="sxs-lookup"><span data-stu-id="cbe93-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="cbe93-143">Теперь приложения должны использовать только **декриптмессаже (NTLM)** .</span><span class="sxs-lookup"><span data-stu-id="cbe93-143">Applications should now use **DecryptMessage (NTLM)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe93-144">Требования</span><span class="sxs-lookup"><span data-stu-id="cbe93-144">Requirements</span></span>

| <span data-ttu-id="cbe93-145">Требование</span><span class="sxs-lookup"><span data-stu-id="cbe93-145">Requirement</span></span> | <span data-ttu-id="cbe93-146">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe93-146">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="cbe93-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbe93-147">Minimum supported client</span></span> | <span data-ttu-id="cbe93-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="cbe93-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbe93-149">Minimum supported server</span></span> | <span data-ttu-id="cbe93-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbe93-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="cbe93-151">Header</span><span class="sxs-lookup"><span data-stu-id="cbe93-151">Header</span></span>                   | <span data-ttu-id="cbe93-152">SSPI. h (включая Security. h)</span><span class="sxs-lookup"><span data-stu-id="cbe93-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="cbe93-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbe93-153">Library</span></span>                  | <span data-ttu-id="cbe93-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="cbe93-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="cbe93-155">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe93-155">DLL</span></span>                      | <span data-ttu-id="cbe93-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="cbe93-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="cbe93-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbe93-157">See also</span></span>

- [<span data-ttu-id="cbe93-158">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="cbe93-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="cbe93-159">**Енкриптмессаже (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="cbe93-159">**EncryptMessage (NTLM)**</span></span>](encryptmessage--ntlm.md)
- [<span data-ttu-id="cbe93-160">**Pvbuffer**</span><span class="sxs-lookup"><span data-stu-id="cbe93-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="cbe93-161">**секбуффердеск**</span><span class="sxs-lookup"><span data-stu-id="cbe93-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
