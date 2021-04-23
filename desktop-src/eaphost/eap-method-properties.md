---
title: Свойства метода EAP (Еаптипес. h)
description: Используется отправителей запросов и методами проверки подлинности для определения методов EAP, которые будут использоваться с конкретными запрашивающими сторонами или средством проверки подлинности. Свойства метода также указывают конфигурацию метода.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802536"
---
# <a name="eap-method-properties"></a><span data-ttu-id="bc3de-104">Свойства метода EAP</span><span class="sxs-lookup"><span data-stu-id="bc3de-104">EAP Method Properties</span></span>

<span data-ttu-id="bc3de-105">Используется отправителей запросов и методами проверки подлинности для определения методов EAP, которые будут использоваться с конкретными запрашивающими сторонами или средством проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bc3de-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="bc3de-106">Свойства метода также указывают конфигурацию метода.</span><span class="sxs-lookup"><span data-stu-id="bc3de-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="bc3de-107">Например, для [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) может потребоваться, чтобы методы имели определенные свойства для использования с [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc3de-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="bc3de-108">Для примера требуется материал для создания ключа.</span><span class="sxs-lookup"><span data-stu-id="bc3de-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="bc3de-109">Перечислены свойства, поддерживаемые методами EAP.</span><span class="sxs-lookup"><span data-stu-id="bc3de-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="bc3de-110">Свойства хранятся в виде значений разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="bc3de-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="bc3de-111">Дополнительные сведения см. в разделе раздел реестра DLL-методов однорангового метода EAP раздела [Конфигурация реестра для методов EAP.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="bc3de-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="bc3de-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**еаппропЦиферсуитенеготиатион**</span><span class="sxs-lookup"><span data-stu-id="bc3de-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc3de-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-114">Метод позволяет согласовать набор шифров с целью шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="bc3de-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="bc3de-115">Windows Server 2008 поддерживает следующие [наборы шифров](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:</span><span class="sxs-lookup"><span data-stu-id="bc3de-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="bc3de-116">TLS \_ RSA \_ с \_ 3DES \_ еде \_ CBC \_ SHA (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="bc3de-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="bc3de-117">TLS \_ дхе \_ DSS \_ с \_ 3DES \_ еде \_ CBC \_ SHA (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="bc3de-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="bc3de-118">SSL \_ CK \_ Des \_ 192 \_ EDE3 \_ CBC \_ WITH \_ MD5 (SSL 2, если включено)</span><span class="sxs-lookup"><span data-stu-id="bc3de-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="bc3de-119">Дополнительные сведения о протоколе безопасности TLS 1,0 см. в [документе RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="bc3de-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**еаппропмутуалаус**</span><span class="sxs-lookup"><span data-stu-id="bc3de-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bc3de-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-122">Метод предоставляет сервер Exchange, в котором средство проверки подлинности проверяет одноранговый узел и наоборот.</span><span class="sxs-lookup"><span data-stu-id="bc3de-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**еаппропинтегрити**</span><span class="sxs-lookup"><span data-stu-id="bc3de-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bc3de-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-125">Метод обеспечивает проверку подлинности источника данных и защиту от несанкционированного изменения информации для пакетов EAP, включая запросы EAP и ответы.</span><span class="sxs-lookup"><span data-stu-id="bc3de-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="bc3de-126">При выполнении этого утверждения спецификация метода должна указывать защищенные пакеты EAP и защищенные поля в пакетах EAP.</span><span class="sxs-lookup"><span data-stu-id="bc3de-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**еаппропреплайпротектион**</span><span class="sxs-lookup"><span data-stu-id="bc3de-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bc3de-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-129">Метод может защититься от воспроизведения метода EAP или его сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc3de-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="bc3de-130">Не удается воспроизвести сообщения о результатах успешного выполнения и сбоя.</span><span class="sxs-lookup"><span data-stu-id="bc3de-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**еаппропконфидентиалити**</span><span class="sxs-lookup"><span data-stu-id="bc3de-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc3de-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-133">Метод может шифровать сообщения EAP.</span><span class="sxs-lookup"><span data-stu-id="bc3de-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="bc3de-134">Запросы EAP, ответы EAP, сообщения о результатах успеха и сообщения об ошибках шифруются.</span><span class="sxs-lookup"><span data-stu-id="bc3de-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="bc3de-135">Метод, который делает это утверждение, должен поддерживать защиту идентификации.</span><span class="sxs-lookup"><span data-stu-id="bc3de-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**еаппропкэйдериватион**</span><span class="sxs-lookup"><span data-stu-id="bc3de-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="bc3de-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-138">Метод может наследовать экспортируемый материал ключа, например главный ключ сеанса (МОСКОВСКОМУ) и ключ расширенного главного сеанса (ЕМСК).</span><span class="sxs-lookup"><span data-stu-id="bc3de-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="bc3de-139">МОСКОВСКОМУ используется только для дальнейшего наследования ключа, а не непосредственно для защиты диалога EAP или последующих данных.</span><span class="sxs-lookup"><span data-stu-id="bc3de-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="bc3de-140">Использование ЕМСК зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="bc3de-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="bc3de-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="bc3de-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-143">Минимальная длина ключа, поддерживаемая методом EAP, — 64 бит.</span><span class="sxs-lookup"><span data-stu-id="bc3de-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="bc3de-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bc3de-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-146">Минимальная длина ключа, поддерживаемая методом EAP, — 128 бит.</span><span class="sxs-lookup"><span data-stu-id="bc3de-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="bc3de-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="bc3de-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-149">Минимальная длина ключа, поддерживаемая методом EAP, — 256 бит.</span><span class="sxs-lookup"><span data-stu-id="bc3de-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="bc3de-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="bc3de-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-152">Минимальная длина ключа, поддерживаемая методом EAP, — 512 бит.</span><span class="sxs-lookup"><span data-stu-id="bc3de-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="bc3de-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="bc3de-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-155">Минимальная длина ключа, поддерживаемая методом EAP, — 1024 бит.</span><span class="sxs-lookup"><span data-stu-id="bc3de-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**еаппропдиктионаряттаккресистанце**</span><span class="sxs-lookup"><span data-stu-id="bc3de-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="bc3de-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-158">Метод не позволяет автономной атаке, имеющей рабочий фактор, в зависимости от числа паролей в словаре злоумышленника.</span><span class="sxs-lookup"><span data-stu-id="bc3de-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="bc3de-159">При использовании проверки подлинности с помощью пароля часто выбираются пароли из небольшого набора (по сравнению с набором N-разрядных ключей), что вызывает проблему при атаках по словарю.</span><span class="sxs-lookup"><span data-stu-id="bc3de-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="bc3de-160">Метод может быть использован для обеспечения защиты от атак из словарей, если, когда он использует пароль в качестве секрета, метод не разрешает автономную атаку, имеющую рабочий фактор на основе числа паролей в словаре злоумышленника.</span><span class="sxs-lookup"><span data-stu-id="bc3de-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**еаппропфастреконнект**</span><span class="sxs-lookup"><span data-stu-id="bc3de-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="bc3de-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-163">Метод имеет возможность (в случае, когда ранее было установлено сопоставление безопасности) для более эффективного создания нового или обновленного сопоставления безопасности или в меньшем количестве обращений.</span><span class="sxs-lookup"><span data-stu-id="bc3de-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**еаппропкриптобиндинг**</span><span class="sxs-lookup"><span data-stu-id="bc3de-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="bc3de-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-166">Метод демонстрирует сервер EAP, что одна сущность действует в качестве однорангового узла EAP для всех методов, выполняемых в туннельном методе.</span><span class="sxs-lookup"><span data-stu-id="bc3de-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="bc3de-167">Привязка может также предположить, что сервер EAP демонстрирует одноранговый узел, что одна сущность использует сервер EAP для всех методов, выполняемых в туннельном методе.</span><span class="sxs-lookup"><span data-stu-id="bc3de-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="bc3de-168">При правильном выполнении Привязка служит для устранения уязвимостей "злоумышленник в середине".</span><span class="sxs-lookup"><span data-stu-id="bc3de-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**еаппропсессиониндепенденце**</span><span class="sxs-lookup"><span data-stu-id="bc3de-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="bc3de-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-171">Метод демонстрирует, что пассивные атаки (например, захват сеанса EAP) или активные атаки (включая атаку МОСКОВСКОМУ или ЕМСК) не нарушают появления последующих или более МСКС или Емскс.</span><span class="sxs-lookup"><span data-stu-id="bc3de-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**еаппропфрагментатион**</span><span class="sxs-lookup"><span data-stu-id="bc3de-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="bc3de-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-174">Метод может поддерживать фрагментацию и сборку, если пакеты EAP превышают минимальное значение MTU (максимальная единица передачи), равное 1020 октетам.</span><span class="sxs-lookup"><span data-stu-id="bc3de-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**еаппропчаннелбиндинг**</span><span class="sxs-lookup"><span data-stu-id="bc3de-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="bc3de-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-177">Метод может передавать Свойства защищенного канала, такие как идентификаторы конечных точек, которые можно сравнивать со значениями, передаваемых с помощью механизмов использования аппаратного контроллера управления, таких как [Проверка подлинности, авторизация, учет](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) или протокол нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="bc3de-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**еаппропнап**</span><span class="sxs-lookup"><span data-stu-id="bc3de-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="bc3de-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="bc3de-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-180">Метод поддерживает защиту доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="bc3de-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**еаппропстандалоне**</span><span class="sxs-lookup"><span data-stu-id="bc3de-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="bc3de-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-183">Метод можно использовать на автономном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc3de-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**еаппропмппинкриптион**</span><span class="sxs-lookup"><span data-stu-id="bc3de-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="bc3de-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="bc3de-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-186">Метод поддерживает шифрование [протокола шифрования "точка — точка" (MPPE)](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="bc3de-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**еаппроптуннелмесод**</span><span class="sxs-lookup"><span data-stu-id="bc3de-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="bc3de-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-189">Метод поддерживает туннелирование других методов EAP.</span><span class="sxs-lookup"><span data-stu-id="bc3de-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**еаппропсуппортсконфиг**</span><span class="sxs-lookup"><span data-stu-id="bc3de-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="bc3de-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-192">Метод поддерживает настраиваемые свойства и имеет пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bc3de-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**еаппропцертифиедмесод**</span><span class="sxs-lookup"><span data-stu-id="bc3de-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="bc3de-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-195">Метод был сертифицирован программой сертификации EAP.</span><span class="sxs-lookup"><span data-stu-id="bc3de-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="bc3de-196">Этот бит должен отправляться только методам EAP, которые прошли сертификацию.</span><span class="sxs-lookup"><span data-stu-id="bc3de-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**еаппропмачинеаус**</span><span class="sxs-lookup"><span data-stu-id="bc3de-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-199">Windows 7 или более поздней версии. метод можно использовать для проверки подлинности компьютера в сети с помощью учетных данных компьютера.</span><span class="sxs-lookup"><span data-stu-id="bc3de-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**еаппропусераус**</span><span class="sxs-lookup"><span data-stu-id="bc3de-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-202">Windows 7 или более поздней версии. метод можно использовать для проверки подлинности пользователя в сети с помощью учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc3de-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**еаппропидентитиприваци**</span><span class="sxs-lookup"><span data-stu-id="bc3de-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-205">Windows 7 или более поздней версии: метод поддерживает отправку удостоверения пользователя в защищенном канале.</span><span class="sxs-lookup"><span data-stu-id="bc3de-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**еаппропмесодчаининг**</span><span class="sxs-lookup"><span data-stu-id="bc3de-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-208">Windows 7 или более поздней версии: метод является туннельным методом и поддерживает цепочку методов EAP в туннеле.</span><span class="sxs-lookup"><span data-stu-id="bc3de-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**еаппропшаредстатикуиваленце**</span><span class="sxs-lookup"><span data-stu-id="bc3de-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-211">Windows 7 или более поздней версии: метод поддерживает эквивалентность общего состояния, как определено в [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span><span class="sxs-lookup"><span data-stu-id="bc3de-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc3de-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**еаппропресервед**</span><span class="sxs-lookup"><span data-stu-id="bc3de-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3de-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="bc3de-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="bc3de-214">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="bc3de-214">Reserved.</span></span> <span data-ttu-id="bc3de-215">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bc3de-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc3de-216">Требования</span><span class="sxs-lookup"><span data-stu-id="bc3de-216">Requirements</span></span>



| <span data-ttu-id="bc3de-217">Требование</span><span class="sxs-lookup"><span data-stu-id="bc3de-217">Requirement</span></span> | <span data-ttu-id="bc3de-218">Значение</span><span class="sxs-lookup"><span data-stu-id="bc3de-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3de-219">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc3de-219">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3de-220">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc3de-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc3de-221">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc3de-221">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3de-222">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc3de-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc3de-223">Header</span><span class="sxs-lookup"><span data-stu-id="bc3de-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc3de-224"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3de-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3de-225">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3de-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3de-226">Разделы реестра для методов EAP</span><span class="sxs-lookup"><span data-stu-id="bc3de-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="bc3de-227">Общие константы EAPHost</span><span class="sxs-lookup"><span data-stu-id="bc3de-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

