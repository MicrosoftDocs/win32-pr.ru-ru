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
ms.openlocfilehash: c88c31d77b666e377cbd1911cde8b5df63d8f5c2fc750cd03a701b03af5b60ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094404"
---
# <a name="eap-method-properties"></a>Свойства метода EAP

Используется отправителей запросов и методами проверки подлинности для определения методов EAP, которые будут использоваться с конкретными запрашивающими сторонами или средством проверки подлинности. Свойства метода также указывают конфигурацию метода.

Например, для [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) может потребоваться, чтобы методы имели определенные свойства для использования с [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) . Для примера требуется материал для создания ключа.

Перечислены свойства, поддерживаемые методами EAP. Свойства хранятся в виде значений разделов реестра. Дополнительные сведения см. в разделе раздел реестра DLL-методов однорангового метода EAP раздела [Конфигурация реестра для методов EAP.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**еаппропЦиферсуитенеготиатион**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Метод позволяет согласовать набор шифров с целью шифрования данных. Windows Сервер 2008 поддерживает следующие [наборы шифров](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:

-   TLS \_ RSA \_ с \_ 3DES \_ еде \_ CBC \_ SHA (TLS & SSL 3)
-   TLS \_ дхе \_ DSS \_ с \_ 3DES \_ еде \_ CBC \_ SHA (TLS & SSL 3)
-   SSL \_ CK \_ Des \_ 192 \_ EDE3 \_ CBC \_ WITH \_ MD5 (SSL 2, если включено)

Дополнительные сведения о протоколе безопасности TLS 1,0 см. в [документе RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**еаппропмутуалаус**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Метод предоставляет сервер Exchange, в котором средство проверки подлинности проверяет одноранговый узел и наоборот.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**еаппропинтегрити**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Метод обеспечивает проверку подлинности источника данных и защиту от несанкционированного изменения информации для пакетов EAP, включая запросы EAP и ответы. При выполнении этого утверждения спецификация метода должна указывать защищенные пакеты EAP и защищенные поля в пакетах EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**еаппропреплайпротектион**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Метод может защититься от воспроизведения метода EAP или его сообщений. Не удается воспроизвести сообщения о результатах успешного выполнения и сбоя.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**еаппропконфидентиалити**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Метод может шифровать сообщения EAP. Запросы EAP, ответы EAP, сообщения о результатах успеха и сообщения об ошибках шифруются. Метод, который делает это утверждение, должен поддерживать защиту идентификации.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**еаппропкэйдериватион**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Метод может наследовать экспортируемый материал ключа, например главный ключ сеанса (МОСКОВСКОМУ) и ключ расширенного главного сеанса (ЕМСК). МОСКОВСКОМУ используется только для дальнейшего наследования ключа, а не непосредственно для защиты диалога EAP или последующих данных. Использование ЕМСК зарезервировано.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Минимальная длина ключа, поддерживаемая методом EAP, — 64 бит.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Минимальная длина ключа, поддерживаемая методом EAP, — 128 бит.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Минимальная длина ключа, поддерживаемая методом EAP, — 256 бит.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Минимальная длина ключа, поддерживаемая методом EAP, — 512 бит.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Минимальная длина ключа, поддерживаемая методом EAP, — 1024 бит.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**еаппропдиктионаряттаккресистанце**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Метод не позволяет автономной атаке, имеющей рабочий фактор, в зависимости от числа паролей в словаре злоумышленника. При использовании проверки подлинности с помощью пароля часто выбираются пароли из небольшого набора (по сравнению с набором N-разрядных ключей), что вызывает проблему при атаках по словарю. Метод может быть использован для обеспечения защиты от атак из словарей, если, когда он использует пароль в качестве секрета, метод не разрешает автономную атаку, имеющую рабочий фактор на основе числа паролей в словаре злоумышленника.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**еаппропфастреконнект**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Метод имеет возможность (в случае, когда ранее было установлено сопоставление безопасности) для более эффективного создания нового или обновленного сопоставления безопасности или в меньшем количестве обращений.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**еаппропкриптобиндинг**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Метод демонстрирует сервер EAP, что одна сущность действует в качестве однорангового узла EAP для всех методов, выполняемых в туннельном методе. Привязка может также предположить, что сервер EAP демонстрирует одноранговый узел, что одна сущность использует сервер EAP для всех методов, выполняемых в туннельном методе. При правильном выполнении Привязка служит для устранения уязвимостей "злоумышленник в середине".


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**еаппропсессиониндепенденце**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Метод демонстрирует, что пассивные атаки (например, захват сеанса EAP) или активные атаки (включая атаку МОСКОВСКОМУ или ЕМСК) не нарушают появления последующих или более МСКС или Емскс.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**еаппропфрагментатион**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Метод может поддерживать фрагментацию и сборку, если пакеты EAP превышают минимальное значение MTU (максимальная единица передачи), равное 1020 октетам.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**еаппропчаннелбиндинг**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Метод может передавать Свойства защищенного канала, такие как идентификаторы конечных точек, которые можно сравнивать со значениями, передаваемых с помощью механизмов использования аппаратного контроллера управления, таких как [Проверка подлинности, авторизация, учет](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) или протокол нижнего уровня.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**еаппропнап**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



Метод поддерживает защиту доступа к сети (NAP).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**еаппропстандалоне**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Метод можно использовать на автономном компьютере.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**еаппропмппинкриптион**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Метод поддерживает шифрование [протокола шифрования "точка — точка" (MPPE)](https://go.microsoft.com/fwlink/p/?linkid=83915) .


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**еаппроптуннелмесод**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Метод поддерживает туннелирование других методов EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**еаппропсуппортсконфиг**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Метод поддерживает настраиваемые свойства и имеет пользовательский интерфейс.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**еаппропцертифиедмесод**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Метод был сертифицирован программой сертификации EAP. Этот бит должен отправляться только методам EAP, которые прошли сертификацию.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**еаппропмачинеаус**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 или более поздней версии. метод можно использовать для проверки подлинности компьютера в сети с помощью учетных данных компьютера.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**еаппропусераус**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 или более поздней версии. метод можно использовать для проверки подлинности пользователя в сети с помощью учетных данных пользователя.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**еаппропидентитиприваци**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 или более поздней версии: метод поддерживает отправку удостоверения пользователя в защищенном канале.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**еаппропмесодчаининг**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 или более поздней версии: метод является туннельным методом и поддерживает цепочку методов EAP в туннеле.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**еаппропшаредстатикуиваленце**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 или более поздней версии: метод поддерживает эквивалентность общего состояния, как определено в [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**еаппропресервед**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Зарезервировано. Не используется.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Еаптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Разделы реестра для методов EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Общие константы EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

