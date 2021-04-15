---
title: Поведение при изменении пароля единого входа
description: Предоставляет пошаговый подход к разрешению изменения пароля единого входа.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105661673"
---
# <a name="sso-password-change-behavior"></a>Поведение при изменении пароля единого входа

В этом разделе приводится пошаговый подход к разрешению изменения пароля единого входа.

## <a name="step-by-step-approach"></a>Пошаговый подход

В следующем списке представлен пошаговый подход к разрешению изменения пароля единого входа.

-   Когда метод EAP получает уведомление об изменении пароля, метод уведомляет EAPHost; В свою очередь, EAPHost уведомляет о обращении, возвращая код действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   После получения кода действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) из EAPHost запрашивающий объект получает контекст пользовательского интерфейса от метода EAP, вызывая функцию [**еафостпиржетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) . Затем EAPHost получает контекст пользовательского интерфейса из метода EAP, вызывая соответствующую функцию метода.
-   Этот объект передает контекст ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в процесс пользовательского интерфейса (используя некоторую форму межпроцессного взаимодействия).
-   Процесс пользовательского интерфейса вызывает [**еафостпиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) для EAPHost.
-   EAPHost собирает контекст пользовательского интерфейса, вызывая [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) для метода EAP.
-   Метод EAP предоставляет все необходимые сведения о контексте пользовательского интерфейса в [**структуре \_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , где *Двдататипе* имеет значение *Еапкредекспирирек* , а *пбуидата* указывает на структуру типа [**EAP \_ cred \_ req**](eap-cred-req.md).
-   При заполнении структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) этот метод EAP заполнит только параметр *куркредс* и не установит флаг " [**\_ \_ PROPS" поля ввода пользовательского интерфейса EAP \_ \_ \_ \_ только для чтения**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) в структуре **\_ \_ \_ \_ данных поля ввода EAP config** .
    > [!Note]  
    > Флаг "Свойства" [**\_ поля ввода пользовательского интерфейса EAP предназначен \_ \_ \_ \_ \_ только для чтения**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) . это поля элементов, которые необходимо изменить.

     

-   Собрав контекст пользовательского интерфейса сведения, процесс пользовательского интерфейса отображает пользовательский интерфейс для сбора сведений об изменении пароля от пользователя. Эти сведения заполняются в параметре *невкредс* структуры [**требований к \_ \_ истечению \_ срока действия EAP-CRED**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .
-   Процесс пользовательского интерфейса передает структуру [**\_ \_ ОТВ**](eap-cred-resp.md) для действия EAP обратно в EAPHost через [**еафостпиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   Процесс пользовательского интерфейса передает этот пользовательский большой двоичный объект объекту-отправитель, и он будет продолжать использовать функции времени выполнения EAPHost как обычно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сценарии для единого входа EAPHost](why-eaphost-sso.md)
</dt> <dt>

[Единый вход и PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




