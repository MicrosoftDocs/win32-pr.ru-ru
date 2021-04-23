---
description: Расшифровывает сообщение с помощью протокола Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Функция Декриптмессаже (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154771"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="fdc5f-103">Функция Декриптмессаже (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="fdc5f-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="fdc5f-104">Функция **декриптмессаже (Kerberos)** расшифровывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="fdc5f-105">Некоторые пакеты не шифруют и не расшифровываются сообщения, а выполняют и проверяют [*хэш*](../secgloss/h-gly.md)целостности.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="fdc5f-106">[**Енкриптмессаже (Kerberos)**](encryptmessage--kerberos.md) и **декриптмессаже (Kerberos)** могут вызываться одновременно из двух разных потоков в одном контексте SSPI, если [*один поток*](../secgloss/s-gly.md) шифруется, а другой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="fdc5f-107">При шифровании нескольких потоков или при расшифровке более одного потока каждый поток должен получить уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc5f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdc5f-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="fdc5f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdc5f-109">Parameters</span></span>

<span data-ttu-id="fdc5f-110">*фконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-110">*phContext* \[in\]</span></span>

<span data-ttu-id="fdc5f-111">Маркер [*контекста безопасности*](../secgloss/s-gly.md) , который будет использоваться для расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="fdc5f-112">*пмессаже* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="fdc5f-113">Указатель на структуру [**секбуффердеск**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="fdc5f-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="fdc5f-114">На входе структура ссылается на одну или несколько структур [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) , которые могут иметь тип данных pvbuffer \_ .</span><span class="sxs-lookup"><span data-stu-id="fdc5f-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="fdc5f-115">Буфер содержит зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="fdc5f-116">Зашифрованное сообщение расшифровывается на месте, переписывая исходное содержимое его буфера.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="fdc5f-117">*Мессажесекно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="fdc5f-118">Порядковый номер, ожидаемый транспортным приложением (при наличии).</span><span class="sxs-lookup"><span data-stu-id="fdc5f-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="fdc5f-119">Если транспортное приложение не поддерживает порядковые номера, этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="fdc5f-120">*пфкоп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="fdc5f-121">Указатель на переменную типа **ulong** , которая получает зависящие от пакета флаги, указывающие качество защиты.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="fdc5f-122">Этот параметр может иметь следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="fdc5f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fdc5f-123">Value</span></span>                  | <span data-ttu-id="fdc5f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fdc5f-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fdc5f-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="fdc5f-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="fdc5f-126">сообщение не было зашифровано, но был создан заголовок или трейлер.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="fdc5f-127">KERB_WRAP_NO_ENCRYPT имеет то же значение и то же самое.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdc5f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdc5f-128">Return value</span></span>

<span data-ttu-id="fdc5f-129">Если функция проверяет, что сообщение было получено в правильной последовательности, функция возвращает значение в секунду \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="fdc5f-130">Если функция не расшифрует сообщение, она возвращает один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="fdc5f-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fdc5f-131">Return code</span></span>                     | <span data-ttu-id="fdc5f-132">Описание</span><span class="sxs-lookup"><span data-stu-id="fdc5f-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc5f-133">**с \_ \_ неполным \_ сообщением электронной почты**</span><span class="sxs-lookup"><span data-stu-id="fdc5f-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="fdc5f-134">Данные во входном буфере неполны.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="fdc5f-135">Приложению необходимо прочитать дополнительные данные с сервера и вызвать [**декриптмессаже (Kerberos)**](decryptmessage--kerberos.md) еще раз.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="fdc5f-136">**с \_ не \_ \_ по \_ порядку**</span><span class="sxs-lookup"><span data-stu-id="fdc5f-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="fdc5f-137">Сообщение не было получено в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="fdc5f-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdc5f-138">Remarks</span></span>

<span data-ttu-id="fdc5f-139">Иногда приложение считывает данные от удаленной стороны, попытается расшифровать их с помощью **декриптмессаже (Kerberos)** и обнаружит, что **декриптмессаже (Kerberos)** закончились, но выходные буферы пусты.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="fdc5f-140">Это нормальное поведение, и приложения должны уметь работать с ним.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="fdc5f-141">Сведения о взаимодействии с GSSAPI см. [в статье взаимодействие между SSPI/Kerberos и GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="fdc5f-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="fdc5f-142">**Windows XP:** Эта функция также называлась **унсеалмессаже**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="fdc5f-143">Теперь приложения должны использовать только **декриптмессаже (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="fdc5f-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc5f-144">Требования</span><span class="sxs-lookup"><span data-stu-id="fdc5f-144">Requirements</span></span>

| <span data-ttu-id="fdc5f-145">Требование</span><span class="sxs-lookup"><span data-stu-id="fdc5f-145">Requirement</span></span> | <span data-ttu-id="fdc5f-146">Значение</span><span class="sxs-lookup"><span data-stu-id="fdc5f-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fdc5f-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdc5f-147">Minimum supported client</span></span> | <span data-ttu-id="fdc5f-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="fdc5f-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdc5f-149">Minimum supported server</span></span> | <span data-ttu-id="fdc5f-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fdc5f-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="fdc5f-151">Header</span><span class="sxs-lookup"><span data-stu-id="fdc5f-151">Header</span></span>                   | <span data-ttu-id="fdc5f-152">SSPI. h (включая Security. h)</span><span class="sxs-lookup"><span data-stu-id="fdc5f-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="fdc5f-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fdc5f-153">Library</span></span>                  | <span data-ttu-id="fdc5f-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="fdc5f-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="fdc5f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc5f-155">DLL</span></span>                      | <span data-ttu-id="fdc5f-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="fdc5f-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="fdc5f-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdc5f-157">See also</span></span>

- [<span data-ttu-id="fdc5f-158">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="fdc5f-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="fdc5f-159">**Енкриптмессаже (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="fdc5f-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="fdc5f-160">**Pvbuffer**</span><span class="sxs-lookup"><span data-stu-id="fdc5f-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="fdc5f-161">**секбуффердеск**</span><span class="sxs-lookup"><span data-stu-id="fdc5f-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
