---
description: Шифрует сообщение для обеспечения конфиденциальности с помощью Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Функция Енкриптмессаже (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272048"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="77e1a-103">Функция Енкриптмессаже (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="77e1a-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="77e1a-104">Функция **енкриптмессаже (Kerberos)** шифрует сообщение для обеспечения [*конфиденциальности*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="77e1a-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="77e1a-105">**Енкриптмессаже (Kerberos)** позволяет приложению выбирать из [*алгоритмов шифрования*](../secgloss/c-gly.md) , поддерживаемых выбранным механизмом.</span><span class="sxs-lookup"><span data-stu-id="77e1a-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="77e1a-106">Функция **енкриптмессаже (Kerberos)** использует [*контекст безопасности*](../secgloss/s-gly.md) , на который ссылается маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="77e1a-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="77e1a-107">Некоторые пакеты не имеют зашифрованных и не расшифрованных сообщений, а предоставляют [*хэш*](../secgloss/h-gly.md) целостности, который можно проверить.</span><span class="sxs-lookup"><span data-stu-id="77e1a-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="77e1a-108">**Енкриптмессаже (Kerberos)** и [**декриптмессаже (Kerberos)**](decryptmessage--kerberos.md) могут вызываться одновременно из двух разных потоков в одном контексте SSPI, если [*один поток*](../secgloss/s-gly.md) шифруется, а другой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="77e1a-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="77e1a-109">При шифровании нескольких потоков или при расшифровке более одного потока каждый поток должен получить уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="77e1a-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e1a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77e1a-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="77e1a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="77e1a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e1a-112">*фконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e1a-113">Маркер [*контекста безопасности*](../secgloss/s-gly.md) , который будет использоваться для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="77e1a-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="77e1a-114">*фкоп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e1a-115">Зависящие от пакета флаги, указывающие качество защиты.</span><span class="sxs-lookup"><span data-stu-id="77e1a-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="77e1a-116">[*Пакет безопасности*](../secgloss/s-gly.md) может использовать этот параметр, чтобы включить выбор [*алгоритмов шифрования*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="77e1a-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="77e1a-117">Этот параметр может иметь следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="77e1a-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="77e1a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="77e1a-118">Value</span></span></th><th><span data-ttu-id="77e1a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="77e1a-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="77e1a-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77e1a-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="77e1a-121">Создать заголовок или трейлер, но не шифровать сообщение.</span><span class="sxs-lookup"><span data-stu-id="77e1a-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="77e1a-122">KERB_WRAP_NO_ENCRYPT имеет то же значение и то же самое.</span><span class="sxs-lookup"><span data-stu-id="77e1a-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="77e1a-123">*пмессаже* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77e1a-124">Указатель на структуру [**секбуффердеск**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="77e1a-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="77e1a-125">На входе структура ссылается на одну или несколько структур [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) , которые могут иметь тип данных pvbuffer \_ .</span><span class="sxs-lookup"><span data-stu-id="77e1a-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="77e1a-126">Этот буфер содержит сообщение для шифрования.</span><span class="sxs-lookup"><span data-stu-id="77e1a-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="77e1a-127">Сообщение шифруется на месте, перезаписывая исходное содержимое структуры.</span><span class="sxs-lookup"><span data-stu-id="77e1a-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="77e1a-128">Функция не обрабатывает буферы с \_ атрибутом pvbuffer ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="77e1a-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="77e1a-129">Длина структуры [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) , содержащей сообщение, не должна превышать **кбмаксимуммессаже**, которая получена из функции [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ attr \_ Streams \_ sizes).</span><span class="sxs-lookup"><span data-stu-id="77e1a-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="77e1a-130">Приложения, не использующие SSL, должны предоставить [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) типа pvbuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="77e1a-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="77e1a-131">*Мессажесекно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e1a-132">Порядковый номер, назначенный сообщению транспортным приложением.</span><span class="sxs-lookup"><span data-stu-id="77e1a-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="77e1a-133">Если транспортное приложение не поддерживает порядковые номера, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="77e1a-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e1a-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77e1a-134">Return value</span></span>

<span data-ttu-id="77e1a-135">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="77e1a-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="77e1a-136">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="77e1a-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="77e1a-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="77e1a-137">Return code</span></span>                                                                                                    | <span data-ttu-id="77e1a-138">Описание</span><span class="sxs-lookup"><span data-stu-id="77e1a-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77e1a-139"><dt>**\_ \_ \_ слишком \_ маленький буфер E с**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="77e1a-140">Выходной буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="77e1a-140">The output buffer is too small.</span></span> <span data-ttu-id="77e1a-141">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="77e1a-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="77e1a-142"><dt>**с \_ \_ \_ истекшим сроком действия в контексте E**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="77e1a-143">Приложение ссылается на контекст, который уже был закрыт.</span><span class="sxs-lookup"><span data-stu-id="77e1a-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="77e1a-144">Правильно написанное приложение не должно получить эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="77e1a-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="77e1a-145"><dt>**с \_ е \_ . \_ неправильная система шифрования E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="77e1a-146">[*Шифр*](../secgloss/c-gly.md) , выбранный для [*контекста безопасности*](../secgloss/s-gly.md) , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="77e1a-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="77e1a-147"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="77e1a-148">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="77e1a-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="77e1a-149"><dt>**c \_ E \_ Недопустимый \_ маркер**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="77e1a-150">В параметре *фконтекст* указан недопустимый маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="77e1a-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="77e1a-151"><dt>**в секунду \_ E \_ Недопустимый \_ токен**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="77e1a-152">Не \_ найден буфер типа данных pvbuffer.</span><span class="sxs-lookup"><span data-stu-id="77e1a-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="77e1a-153"><dt>**с \_ е \_ КОП \_ не \_ поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="77e1a-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="77e1a-154">[*Контекст безопасности*](../secgloss/s-gly.md)не поддерживает ни конфиденциальность, ни [*целостность*](../secgloss/i-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="77e1a-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="77e1a-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77e1a-155">Remarks</span></span>

<span data-ttu-id="77e1a-156">Функция **енкриптмессаже (Kerberos)** шифрует сообщение на основе сообщения и [*ключа сеанса*](../secgloss/s-gly.md) из [*контекста безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="77e1a-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="77e1a-157">Если приложение транспорта создало [*контекст безопасности*](../secgloss/s-gly.md) для поддержки обнаружения последовательности и вызывающий объект предоставляет порядковый номер, функция включает эти сведения в зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="77e1a-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="77e1a-158">Включение этой информации обеспечивает защиту от воспроизведения, вставки и подавления сообщений.</span><span class="sxs-lookup"><span data-stu-id="77e1a-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="77e1a-159">[*Пакет безопасности*](../secgloss/s-gly.md) включает порядковый номер, переданный из транспортного приложения.</span><span class="sxs-lookup"><span data-stu-id="77e1a-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="77e1a-160">Эти буферы должны быть представлены в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="77e1a-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="77e1a-161">Тип буфера</span><span class="sxs-lookup"><span data-stu-id="77e1a-161">Buffer type</span></span>                           | <span data-ttu-id="77e1a-162">Описание</span><span class="sxs-lookup"><span data-stu-id="77e1a-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e1a-163">\_ \_< заголовка потока pvbuffer</span><span class="sxs-lookup"><span data-stu-id="77e1a-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="77e1a-164">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="77e1a-164">Used internally.</span></span> <span data-ttu-id="77e1a-165">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="77e1a-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="77e1a-166">\_данные pvbuffer</span><span class="sxs-lookup"><span data-stu-id="77e1a-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="77e1a-167">Содержит зашифрованное сообщение в [*виде открытого текста*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="77e1a-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="77e1a-168">\_трейлер потока \_ pvbuffer</span><span class="sxs-lookup"><span data-stu-id="77e1a-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="77e1a-169">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="77e1a-169">Used internally.</span></span> <span data-ttu-id="77e1a-170">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="77e1a-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="77e1a-171">PVBUFFER \_ пусто</span><span class="sxs-lookup"><span data-stu-id="77e1a-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="77e1a-172">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="77e1a-172">Used internally.</span></span> <span data-ttu-id="77e1a-173">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="77e1a-173">No initialization required.</span></span> <span data-ttu-id="77e1a-174">Размер может быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="77e1a-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="77e1a-175">Для оптимальной производительности структуры *пмессаже* должны выделяться из непрерывной памяти.</span><span class="sxs-lookup"><span data-stu-id="77e1a-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="77e1a-176">**Windows XP:** Эта функция также называлась **сеалмессаже**.</span><span class="sxs-lookup"><span data-stu-id="77e1a-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="77e1a-177">Теперь приложения должны использовать только **енкриптмессаже (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="77e1a-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e1a-178">Требования</span><span class="sxs-lookup"><span data-stu-id="77e1a-178">Requirements</span></span>

| <span data-ttu-id="77e1a-179">Требование</span><span class="sxs-lookup"><span data-stu-id="77e1a-179">Requirement</span></span> | <span data-ttu-id="77e1a-180">Значение</span><span class="sxs-lookup"><span data-stu-id="77e1a-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="77e1a-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77e1a-181">Minimum supported client</span></span> | <span data-ttu-id="77e1a-182">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="77e1a-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77e1a-183">Minimum supported server</span></span> | <span data-ttu-id="77e1a-184">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77e1a-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="77e1a-185">Header</span><span class="sxs-lookup"><span data-stu-id="77e1a-185">Header</span></span>                   | <span data-ttu-id="77e1a-186">SSPI. h (включая Security. h)</span><span class="sxs-lookup"><span data-stu-id="77e1a-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="77e1a-187">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77e1a-187">Library</span></span>                  | <span data-ttu-id="77e1a-188">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="77e1a-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="77e1a-189">DLL</span><span class="sxs-lookup"><span data-stu-id="77e1a-189">DLL</span></span>                      | <span data-ttu-id="77e1a-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="77e1a-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="77e1a-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77e1a-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e1a-192">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="77e1a-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="77e1a-193">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="77e1a-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="77e1a-194">**Декриптмессаже (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="77e1a-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="77e1a-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="77e1a-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="77e1a-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="77e1a-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="77e1a-197">**Pvbuffer**</span><span class="sxs-lookup"><span data-stu-id="77e1a-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="77e1a-198">**секбуффердеск**</span><span class="sxs-lookup"><span data-stu-id="77e1a-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
