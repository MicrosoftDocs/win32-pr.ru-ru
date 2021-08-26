---
title: Реализация поддержки NAP для методов EAP
description: Узнайте, как реализовать поддержку NAP для запрашивающего устройства EAPHost. См. разделы, посвященные защите доступа к версии EAPHost, и просмотрите дополнительные доступные ресурсы.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00860057baeedbfdbae1939ab402db6f28fd74bd
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812389"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Реализация поддержки NAP для методов EAP

В этом разделе объясняется, как реализовать NAP для запрашивающего устройства EAPHost. в Windows Vista и Windows Server 2008 клиент принудительной защиты доступа к сети (nap EC) доступен для подключений с проверкой подлинности [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .

## <a name="implementing-network-access-protection-nap"></a>Реализация защиты доступа к сети (NAP)

Для поддержки NAP в качестве запрашивающего объекта EAPHost реализуется функция обратного вызова, соответствующая прототипу обратного вызова [**нотификатионхандлер**](/previous-versions/windows/desktop/api) , и при вызове [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)необходимо предоставить указатель на эту функцию обратного вызова.

Функция обратного вызова принимает два параметра.

-   Идентификатор GUID, однозначно определяющий интерфейс, связанный с проверкой подлинности.
-   Указатель типа VOID на непрозрачную структуру данных, предоставляемую вызывающим объектом.

Функция EAPHost вызывает предоставленную через вызывающую сторона функцию обратного вызова с уникальным идентификатором GUID интерфейса и указателем VOID при изменении состояния карантина компьютера. Когда EAPHost вызывает функцию обратного вызова, предоставленную вызывающим объектом, он реагирует на то, что логическое сетевое подключение, определяемое указателем GUID/VOID интерфейса, и снова начинает проверку подлинности с помощью **еафостпирбегинсессион**.

EAPHost может вызвать функцию обратного вызова, предоставленную через вызывающий объект, в любое время: до, во время активной проверки подлинности или после завершения проверки подлинности (после вызова [**еафостпирендсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) , но не до вызова [**еафостпирклеарконнектион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ). Он должен всегда отвечать на запросы путем разрыва подключения логической сети и повторной проверки подлинности.

Если вызывающий объект завершает работу или не получает уведомления об изменениях состояния изоляции, он должен вызвать [**еафостпирклеарконнектион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) и указать соответствующий GUID интерфейса. Если необходимо определить изоляцию логического сетевого подключения, он может получить эту информацию из **еафостпирмесодресулт. исолатионстате** , когда [**Еафостпирмесодресулт**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) получен из [**еафостпиржетресулт**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Сведения о NAP, связанные с EAPHost

Сведения о NAP, связанные с API EAPHost, см. в следующих разделах.

-   [**\_тип атрибута \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**\_ошибка EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Часто задаваемые вопросы о запрашивающем сторона EAPHost](eaphost-supplicant-frequently-asked-questions.yml)
-   [**Свойства метода EAP**](eap-method-properties.md)
-   [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Константы, относящиеся к EAP и сведения об ошибках**](eap-related-error-and-information-constants.md)
-   [**\_состояние изоляции**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**нотификатионхандлер**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Дополнительные ресурсы


-   Список ресурсов NAP см. в разделе [Защита доступа к сети](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Сведения о состоянии работоспособности см. в разделе сообщения о состоянии [работоспособности защиты доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   сведения о веб-странице Enterprise networking Group и блоге см. в разделе [защита доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Сведения об API NAP см. в разделе [Защита доступа к сети](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка пользовательского интерфейса метода EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Включение групповая политика](enabling-group-policy.md)
</dt> <dt>

[Реализация поддержки NAP In-Band для методов EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Передача данных между запрашивающим и методами EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost отправителей запросов](eaphost-supplicants.md)
</dt> </dl>

 

 