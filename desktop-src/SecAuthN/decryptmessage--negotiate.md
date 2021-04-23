---
description: Расшифровывает сообщение с помощью Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Функция Декриптмессаже (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719364"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="ace82-103">Функция Декриптмессаже (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="ace82-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="ace82-104">Функция **декриптмессаже (Negotiate)** расшифровывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="ace82-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="ace82-105">Некоторые пакеты не шифруют и не расшифровываются сообщения, а выполняют и проверяют [*хэш*](../secgloss/h-gly.md)целостности.</span><span class="sxs-lookup"><span data-stu-id="ace82-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="ace82-106">[**Енкриптмессаже (Negotiate)**](encryptmessage--negotiate.md) и **декриптмессаже (Negotiate)** могут быть вызваны одновременно из двух разных потоков в одном контексте SSPI, [*Если один поток*](../secgloss/s-gly.md) шифруется, а другой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="ace82-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="ace82-107">При шифровании нескольких потоков или при расшифровке более одного потока каждый поток должен получить уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="ace82-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace82-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="ace82-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace82-109">Parameters</span></span>

<span data-ttu-id="ace82-110">*фконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace82-110">*phContext* \[in\]</span></span>

<span data-ttu-id="ace82-111">Маркер [*контекста безопасности*](../secgloss/s-gly.md) , который будет использоваться для расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ace82-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="ace82-112">*пмессаже* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ace82-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="ace82-113">Указатель на структуру [**секбуффердеск**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="ace82-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="ace82-114">На входе структура ссылается на одну или несколько структур [**pvbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ace82-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="ace82-115">По крайней мере один из них должен иметь тип \_ данных pvbuffer.</span><span class="sxs-lookup"><span data-stu-id="ace82-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="ace82-116">Этот буфер содержит зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="ace82-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="ace82-117">Зашифрованное сообщение расшифровывается на месте, переписывая исходное содержимое его буфера.</span><span class="sxs-lookup"><span data-stu-id="ace82-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="ace82-118">*Мессажесекно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace82-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="ace82-119">Порядковый номер, ожидаемый транспортным приложением (при наличии).</span><span class="sxs-lookup"><span data-stu-id="ace82-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="ace82-120">Если транспортное приложение не поддерживает порядковые номера, этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="ace82-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="ace82-121">*пфкоп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ace82-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="ace82-122">Указатель на переменную типа **ulong** , которая получает зависящие от пакета флаги, указывающие качество защиты.</span><span class="sxs-lookup"><span data-stu-id="ace82-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="ace82-123">Этот параметр может иметь следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="ace82-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="ace82-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ace82-124">Value</span></span></th><th><span data-ttu-id="ace82-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ace82-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="ace82-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ace82-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="ace82-127">Сообщение не было зашифровано, но был создан заголовок или трейлер.</span><span class="sxs-lookup"><span data-stu-id="ace82-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="ace82-128">KERB_WRAP_NO_ENCRYPT имеет то же значение и то же самое.</span><span class="sxs-lookup"><span data-stu-id="ace82-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="ace82-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ace82-129">Return value</span></span>

<span data-ttu-id="ace82-130">Если функция проверяет, что сообщение было получено в правильной последовательности, функция возвращает значение в секунду \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ace82-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="ace82-131">Если функция не расшифрует сообщение, она возвращает один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="ace82-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="ace82-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ace82-132">Return code</span></span>                     | <span data-ttu-id="ace82-133">Описание</span><span class="sxs-lookup"><span data-stu-id="ace82-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace82-134">**с \_ \_ неполным \_ сообщением электронной почты**</span><span class="sxs-lookup"><span data-stu-id="ace82-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="ace82-135">Данные во входном буфере неполны.</span><span class="sxs-lookup"><span data-stu-id="ace82-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="ace82-136">Приложению необходимо прочитать больше данных с сервера и снова вызвать [**декриптмессаже (Negotiate)**](decryptmessage--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="ace82-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="ace82-137">**с \_ не \_ \_ по \_ порядку**</span><span class="sxs-lookup"><span data-stu-id="ace82-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="ace82-138">Сообщение не было получено в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="ace82-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="ace82-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ace82-139">Remarks</span></span>

<span data-ttu-id="ace82-140">Иногда приложение будет считывать данные от удаленной стороны, пытаться расшифровать их с помощью **декриптмессаже (Negotiate)**, а также обнаружить, что **декриптмессаже (Negotiate)** закончились, но выходные буферы пусты.</span><span class="sxs-lookup"><span data-stu-id="ace82-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="ace82-141">Это нормальное поведение, и приложения должны уметь работать с ним.</span><span class="sxs-lookup"><span data-stu-id="ace82-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="ace82-142">**Windows XP:** Эта функция также называлась **унсеалмессаже**.</span><span class="sxs-lookup"><span data-stu-id="ace82-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="ace82-143">Теперь приложения должны использовать только **декриптмессаже (Negotiate)** .</span><span class="sxs-lookup"><span data-stu-id="ace82-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace82-144">Требования</span><span class="sxs-lookup"><span data-stu-id="ace82-144">Requirements</span></span>

| <span data-ttu-id="ace82-145">Требование</span><span class="sxs-lookup"><span data-stu-id="ace82-145">Requirement</span></span> | <span data-ttu-id="ace82-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ace82-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ace82-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ace82-147">Minimum supported client</span></span> | <span data-ttu-id="ace82-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ace82-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="ace82-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ace82-149">Minimum supported server</span></span> | <span data-ttu-id="ace82-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ace82-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="ace82-151">Header</span><span class="sxs-lookup"><span data-stu-id="ace82-151">Header</span></span>                   | <span data-ttu-id="ace82-152">SSPI. h (включая Security. h)</span><span class="sxs-lookup"><span data-stu-id="ace82-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="ace82-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ace82-153">Library</span></span>                  | <span data-ttu-id="ace82-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="ace82-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="ace82-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ace82-155">DLL</span></span>                      | <span data-ttu-id="ace82-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="ace82-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="ace82-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace82-157">See also</span></span>

- [<span data-ttu-id="ace82-158">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="ace82-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="ace82-159">**Енкриптмессаже (согласование)**</span><span class="sxs-lookup"><span data-stu-id="ace82-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="ace82-160">**Pvbuffer**</span><span class="sxs-lookup"><span data-stu-id="ace82-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="ace82-161">**секбуффердеск**</span><span class="sxs-lookup"><span data-stu-id="ace82-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
