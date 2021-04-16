---
description: Шифрует сообщение для обеспечения конфиденциальности с помощью дайджеста.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Функция Енкриптмессаже (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719301"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="70367-103">Функция Енкриптмессаже (Digest)</span><span class="sxs-lookup"><span data-stu-id="70367-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="70367-104">Функция **енкриптмессаже (Digest)** шифрует сообщение для обеспечения [*конфиденциальности*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70367-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="70367-105">**Енкриптмессаже (дайджест)** позволяет приложению выбирать между [*алгоритмами шифрования*](../secgloss/c-gly.md) , поддерживаемыми выбранным механизмом.</span><span class="sxs-lookup"><span data-stu-id="70367-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="70367-106">Функция **енкриптмессаже (Digest)** использует [*контекст безопасности*](../secgloss/s-gly.md) , на который ссылается маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="70367-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="70367-107">Некоторые пакеты не имеют зашифрованных и не расшифрованных сообщений, а предоставляют [*хэш*](../secgloss/h-gly.md) целостности, который можно проверить.</span><span class="sxs-lookup"><span data-stu-id="70367-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="70367-108">Эта функция доступна только в качестве механизма SASL.</span><span class="sxs-lookup"><span data-stu-id="70367-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="70367-109">**Енкриптмессаже (дайджест)** и [**декриптмессаже (Digest)**](decryptmessage--digest.md) могут быть вызваны одновременно из двух разных потоков в одном контексте [*интерфейса поставщика услуг обеспечения безопасности*](../secgloss/s-gly.md) (SSPI), если один поток шифруется, а другой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="70367-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="70367-110">При шифровании нескольких потоков или при расшифровке более одного потока каждый поток должен получить уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="70367-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="70367-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70367-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="70367-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="70367-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70367-113">*фконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70367-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70367-114">Маркер [*контекста безопасности*](../secgloss/s-gly.md) , который будет использоваться для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="70367-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="70367-115">*фкоп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70367-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70367-116">Зависящие от пакета флаги, указывающие качество защиты.</span><span class="sxs-lookup"><span data-stu-id="70367-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="70367-117">[*Пакет безопасности*](../secgloss/s-gly.md) может использовать этот параметр, чтобы включить выбор [*алгоритмов шифрования*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70367-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="70367-118">При использовании дайджест-поставщика общих служб этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="70367-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="70367-119">*пмессаже* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="70367-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70367-120">Указатель на структуру [**секбуффердеск**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="70367-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="70367-121">На входе структура ссылается на одну или несколько структур [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) , которые могут иметь тип данных pvbuffer \_ .</span><span class="sxs-lookup"><span data-stu-id="70367-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="70367-122">Этот буфер содержит сообщение для шифрования.</span><span class="sxs-lookup"><span data-stu-id="70367-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="70367-123">Сообщение шифруется на месте, перезаписывая исходное содержимое структуры.</span><span class="sxs-lookup"><span data-stu-id="70367-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="70367-124">Функция не обрабатывает буферы с \_ атрибутом pvbuffer ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="70367-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="70367-125">Длина структуры [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) , которая содержит сообщение, должна быть не больше **кбмаксимуммессаже**, полученной из функции [**QueryContextAttributes (дайджест)**](querycontextattributes--digest.md) (SECPKG \_ attr \_ Streams \_ sizes).</span><span class="sxs-lookup"><span data-stu-id="70367-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="70367-126">При использовании дайджест-поставщика общих служб \_ \_ \_ для хранения сведений о [*сигнатурах*](../secgloss/d-gly.md#_security_digital_signature_gly) должен быть второй буфер с типом заполнения pvbuffer или с данными буфера (в секунду).</span><span class="sxs-lookup"><span data-stu-id="70367-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="70367-127">Чтобы получить размер выходного буфера, вызовите функцию [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) и укажите \_ размеры SECPKG attr \_ .</span><span class="sxs-lookup"><span data-stu-id="70367-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="70367-128">Функция вернет структуру [**\_ размеров секпкгконтекст**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="70367-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="70367-129">Размер выходного буфера равен сумме значений в элементах **кбмакссигнатуре** и **кбблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="70367-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="70367-130">Приложения, не использующие SSL, должны предоставить [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) типа pvbuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="70367-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="70367-131">*Мессажесекно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70367-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70367-132">Порядковый номер, назначенный сообщению транспортным приложением.</span><span class="sxs-lookup"><span data-stu-id="70367-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="70367-133">Если транспортное приложение не поддерживает порядковые номера, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="70367-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="70367-134">При использовании дайджест-поставщика общих служб этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="70367-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="70367-135">Хэш-код дайджеста управляет нумерацией последовательности внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="70367-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70367-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70367-136">Return value</span></span>

<span data-ttu-id="70367-137">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="70367-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="70367-138">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="70367-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="70367-139">Код возврата</span><span class="sxs-lookup"><span data-stu-id="70367-139">Return code</span></span>                                                                                                    | <span data-ttu-id="70367-140">Описание</span><span class="sxs-lookup"><span data-stu-id="70367-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70367-141"><dt>**\_ \_ \_ слишком \_ маленький буфер E с**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="70367-142">Выходной буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="70367-142">The output buffer is too small.</span></span> <span data-ttu-id="70367-143">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="70367-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="70367-144"><dt>**с \_ \_ \_ истекшим сроком действия в контексте E**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="70367-145">Приложение ссылается на контекст, который уже был закрыт.</span><span class="sxs-lookup"><span data-stu-id="70367-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="70367-146">Правильно написанное приложение не должно получить эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="70367-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="70367-147"><dt>**с \_ е \_ . \_ неправильная система шифрования E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="70367-148">[*Шифр*](../secgloss/c-gly.md) , выбранный для [*контекста безопасности*](../secgloss/s-gly.md) , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="70367-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="70367-149"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="70367-150">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="70367-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="70367-151"><dt>**c \_ E \_ Недопустимый \_ маркер**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="70367-152">В параметре *фконтекст* указан недопустимый маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="70367-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="70367-153"><dt>**в секунду \_ E \_ Недопустимый \_ токен**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="70367-154">Не \_ найден буфер типа данных pvbuffer.</span><span class="sxs-lookup"><span data-stu-id="70367-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="70367-155"><dt>**с \_ е \_ КОП \_ не \_ поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="70367-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="70367-156">[*Контекст безопасности*](../secgloss/s-gly.md)не поддерживает ни конфиденциальность, ни [*целостность*](../secgloss/i-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="70367-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70367-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70367-157">Remarks</span></span>

<span data-ttu-id="70367-158">Функция **енкриптмессаже (Digest)** шифрует сообщение на основе сообщения и [*ключа сеанса*](../secgloss/s-gly.md) из [*контекста безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70367-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="70367-159">Если приложение транспорта создало [*контекст безопасности*](../secgloss/s-gly.md) для поддержки обнаружения последовательности и вызывающий объект предоставляет порядковый номер, функция включает эти сведения в зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="70367-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="70367-160">Включение этой информации обеспечивает защиту от воспроизведения, вставки и подавления сообщений.</span><span class="sxs-lookup"><span data-stu-id="70367-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="70367-161">[*Пакет безопасности*](../secgloss/s-gly.md) включает порядковый номер, переданный из транспортного приложения.</span><span class="sxs-lookup"><span data-stu-id="70367-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="70367-162">При использовании дайджест-поставщика общих служб получите размер выходного буфера, вызвав функцию [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) и УКАЗАВ \_ размеры SECPKG attr \_ .</span><span class="sxs-lookup"><span data-stu-id="70367-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="70367-163">Функция вернет структуру [**\_ размеров секпкгконтекст**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="70367-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="70367-164">Размер выходного буфера равен сумме значений в элементах **кбмакссигнатуре** и **кбблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="70367-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="70367-165">Эти буферы должны быть представлены в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="70367-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="70367-166">Тип буфера</span><span class="sxs-lookup"><span data-stu-id="70367-166">Buffer type</span></span>                           | <span data-ttu-id="70367-167">Описание</span><span class="sxs-lookup"><span data-stu-id="70367-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70367-168">\_заголовок потока \_ pvbuffer</span><span class="sxs-lookup"><span data-stu-id="70367-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="70367-169">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="70367-169">Used internally.</span></span> <span data-ttu-id="70367-170">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="70367-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="70367-171">\_данные pvbuffer</span><span class="sxs-lookup"><span data-stu-id="70367-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="70367-172">Содержит зашифрованное сообщение в [*виде открытого текста*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="70367-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="70367-173">\_трейлер потока \_ pvbuffer</span><span class="sxs-lookup"><span data-stu-id="70367-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="70367-174">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="70367-174">Used internally.</span></span> <span data-ttu-id="70367-175">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="70367-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="70367-176">PVBUFFER \_ пусто</span><span class="sxs-lookup"><span data-stu-id="70367-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="70367-177">Для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="70367-177">Used internally.</span></span> <span data-ttu-id="70367-178">Инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="70367-178">No initialization required.</span></span> <span data-ttu-id="70367-179">Размер может быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="70367-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="70367-180">Для оптимальной производительности структуры *пмессаже* должны выделяться из непрерывной памяти.</span><span class="sxs-lookup"><span data-stu-id="70367-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="70367-181">**Windows XP:** Эта функция также называлась **сеалмессаже**.</span><span class="sxs-lookup"><span data-stu-id="70367-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="70367-182">Теперь приложения должны использовать только **енкриптмессаже (дайджест)** .</span><span class="sxs-lookup"><span data-stu-id="70367-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="70367-183">Требования</span><span class="sxs-lookup"><span data-stu-id="70367-183">Requirements</span></span>



| <span data-ttu-id="70367-184">Требование</span><span class="sxs-lookup"><span data-stu-id="70367-184">Requirement</span></span> | <span data-ttu-id="70367-185">Значение</span><span class="sxs-lookup"><span data-stu-id="70367-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70367-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70367-186">Minimum supported client</span></span><br/> | <span data-ttu-id="70367-187">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="70367-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="70367-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70367-188">Minimum supported server</span></span><br/> | <span data-ttu-id="70367-189">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70367-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="70367-190">Header</span><span class="sxs-lookup"><span data-stu-id="70367-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="70367-191"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70367-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="70367-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="70367-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="70367-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70367-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="70367-194">DLL</span><span class="sxs-lookup"><span data-stu-id="70367-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70367-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70367-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="70367-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70367-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70367-197">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="70367-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="70367-198">**AcceptSecurityContext (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="70367-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="70367-199">**Декриптмессаже (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="70367-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="70367-200">**InitializeSecurityContext (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="70367-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="70367-201">**QueryContextAttributes (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="70367-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="70367-202">**Pvbuffer**</span><span class="sxs-lookup"><span data-stu-id="70367-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="70367-203">**секбуффердеск**</span><span class="sxs-lookup"><span data-stu-id="70367-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
