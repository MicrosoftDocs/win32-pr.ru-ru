---
title: Включение групповая политика
description: Узнайте, как настроить этот метод, включив групповую политику. См. раздел рекомендации по отправителей запросов и Просмотр дополнительных доступных ресурсов.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a36d2d464ef4f29c1f021f5ee7d1fad4d820e5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812729"
---
# <a name="enabling-group-policy"></a>Включение групповая политика

В этом разделе объясняется, как настроить вызывающий объект, включив групповую политику. EAPHost отправителей запросов может участвовать в групповой политике, чтобы администратор сети мог централизованно настраивать свои сетевые компьютеры.

Точный метод и механизм, с помощью которых запрашивающая сторона принимает участие в групповой политике, — это по усмотрению запрашивающей стороны. Примеры механизмов для участия в групповой политике включают расширения клиент-сервер, административный шаблон и т. д.

## <a name="considerations-when-enabling-group-policy"></a>Рекомендации по включению групповая политика

Ниже приведены рекомендации по отправителей запросов в отношении групповой политики и EAP.

1.  Конфигурация EAP всегда должна храниться в формате XML везде, где это возможно, а не в двоичном формате. Групповая политика может быть применена к любому компьютеру в домене, а конфигурация метода EAP и данные пользователя не гарантированно переносимы между архитектурой 32-разрядных и 64-разрядных процессоров. XML разрешает проблемы с границами архитектуры процессора, так как запрашивающая сторона локально преобразует независимый XML-код архитектуры процессора в двоичное представление конфигурации во время проверки подлинности.

    Дополнительные сведения см. в следующих статьях.

    -   [Общие вопросы и ответы](general-frequently-asked-questions.yml)
    -   [Метод EAP часто задаваемые вопросы](eap-method-frequently-asked-questions.yml).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Если используется расширение на стороне сервера групповой политики, то расширение будет вызывать [**еафостпиржетмесодс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) , как правило, для определения доступных методов и создания соответствующей конфигурации EAP для этой политики. Затем политика отправляется на соответствующие сетевые клиенты, где применяется политика.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка пользовательского интерфейса метода EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Реализация поддержки NAP In-Band для методов EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Реализация поддержки NAP для методов EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Передача данных между запрашивающим и методами EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost отправителей запросов](eaphost-supplicants.md)
</dt> </dl>

 

 




