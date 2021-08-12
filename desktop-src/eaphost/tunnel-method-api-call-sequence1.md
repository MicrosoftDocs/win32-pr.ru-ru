---
title: Tunnel Последовательность вызовов API метода
description: сведения о последовательности вызовов API для Tunnel методов. См. Обзор и Просмотр дополнительных доступных ресурсов.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca32a889229b6cdbdb3f008ebea8b838f9b6d64fba36bc2a30c4ddd9d62ac83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272800"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Последовательность вызовов API метода

в этом разделе рассматривается последовательность вызовов API для Tunnel методов.

## <a name="tunnel-method-call-sequence-overview"></a>Tunnel Общие сведения о последовательности вызовов методов

Когда запрашивающая сторона получает запрос на удостоверение пользователя и данные пользователя, обычно возникает следующий поток вызова API.

-   Запрашивающий объект вызывает Еафостпирпроцессрецеиведпаккет в EapHost для обработки пакета, полученного от средства проверки подлинности.
-   После обработки этого пакета EAPHost определяет его как пакет Идентитирекуест и вызывает [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) в методе Tunnel, чтобы получить удостоверение пользователя, используемое для проверки подлинности.
-   Если методу туннелирования необходимо получить удостоверение пользователя из внутреннего метода, он вызывает [**еафостпиржетидентити**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) для внутреннего метода EAPHost, который, в свою очередь, вызывает [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) во внутреннем методе.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>взаимодействие пользователя с вызовом API Tunnel methods Flow

В некоторых случаях, когда удостоверение недоступно или пользователь должен предоставить дополнительные сведения, метод EAP выдает диалоговое окно пользовательского интерфейса на вызывающий объект.

В таких случаях для получения сведений непосредственно от пользователя обычно используется последовательность вызовов.

-   Tunnel Метод EAP возвращает код действия для вызова пользовательского интерфейса в EapHost. Запрашивающий объект вызывает [**еафостпиржетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)для получения сведений о текущем контексте пользовательского интерфейса для диалогового окна пользовательского интерфейса.
-   Затем запрашивающий метод вызывает [ **еафостпиринвокеинтерактивеуи.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Эта функция использует сведения о контексте пользовательского интерфейса для вызова интерактивного пользовательского интерфейса, который используется для получения учетных данных от пользователя. Процесс пользовательского интерфейса загружает Eappcfg.dll и получает указатели на Еаппиринвокеинтерактивеуи и Еаппирфримемори.
    > [!Note]  
    > Процесс пользовательского интерфейса обычно собирает пользовательский интерфейс или обрабатывает интерактивный пользовательский интерфейс и отделен от процесса запрашивающего устройства. Разделение этих двух процессов не является требованием EAPHost, но это имеет преимущество, позволяя процессу пользовательского интерфейса взаимодействовать с рабочим столом.

     

-   EapHost вызывает [**еаппиринвокеидентитюи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) в методе Tunnel для получения сведений об удостоверении пользователя.
-   Чтобы получить удостоверение пользователя из внутреннего метода, метод туннеля вызывает [**еафостпиринвокеидентитюи**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) для внутренней EAPHost.
-   Внутренняя метод EAPHost вызывает [**еаппиринвокеидентитюи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) для внутреннего метода для вызова пользовательского интерфейса удостоверения пользователя.
-   [**Еафостпирсетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) предоставляет новые или обновленные сведения о контексте пользовательского интерфейса для однорангового метода EAP, загруженного в EAPHost после создания пользовательского интерфейса.

на следующей схеме объясняется последовательность вызовов API для Tunnel методов.

![последовательность вызовов API методов туннеля](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Последовательность вызовов EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Последовательность вызовов API-интерфейса для запрашивающих сторон](supplicant-api-call-sequence.md)
</dt> <dt>

[Справочник по API для запрашивающей сторона EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




