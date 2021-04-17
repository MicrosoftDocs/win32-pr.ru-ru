---
title: Часто задаваемые вопросы о методе EAP
description: Содержит ответы на часто задаваемые вопросы по программированию методов EAP.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105691694"
---
# <a name="eap-method-frequently-asked-questions"></a>Часто задаваемые вопросы о методе EAP

Этот раздел содержит ответы на часто задаваемые вопросы о разработке методов EAP.

## <a name="eap-method-frequently-asked-questions"></a>Часто задаваемые вопросы о методе EAP



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Вопрос</th>
<th>Ответ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Что такое &quot; данные конфигурации &quot; ?</td>
<td>Термины &quot; данные конфигурации &quot; и &quot; данные соединения &quot; являются синонимами.</td>
</tr>
<tr class="even">
<td>Что такое &quot; данные подключения &quot; ?</td>
<td>&quot;Данные соединения &quot; — это непрозрачный большой двоичный объект, относящийся к методу EAP, который содержит сведения о конфигурации для метода. Эти данные соединения создаются методом при первоначальной настройке и никогда не обрабатываются или не изменяются каким-либо другим компонентом, чем сам метод EAP.</td>
</tr>
<tr class="odd">
<td>Что такое &quot; учетные данные &quot; ?</td>
<td>Термины &quot; учетные данные &quot; и &quot; данные пользователя &quot; являются синонимами.</td>
</tr>
<tr class="even">
<td>Что такое &quot; данные пользователя &quot; ?</td>
<td>&quot;Данные пользователя &quot; — это непрозрачный большой двоичный объект, зависящий от метода EAP, который содержит данные учетных данных пользователя, такие как имя пользователя и пароль. Пользовательские данные никогда не обрабатываются или не изменяются каким-либо другим компонентом, чем сам метод EAP. Термины &quot; пользовательские данные &quot; и &quot; учетные данные &quot; являются синонимами.</td>
</tr>
<tr class="odd">
<td>Что такое &quot; атрибут EAP &quot; ?</td>
<td>&quot;Атрибут EAP &quot; — это структура данных, которая содержит предварительно определенный тип данных. Атрибуты используются для обмена данными между методами EAP и отправителей запросов, а также между методами и проверками подлинности EAP. Реализации метода EAP в одноранговых сетях и средствах проверки подлинности могут обмениваться этими атрибутами по сети.</td>
</tr>
<tr class="even">
<td>Может ли API конфигурации и API времени выполнения отображаться в одной и той же библиотеке DLL метода?</td>
<td>Да. Не забудьте указать различие при настройке записей реестра для самого метода EAP. Путь конфигурации и путь однорангового узла должны быть одинаковыми.</td>
</tr>
<tr class="odd">
<td>Могут ли API конфигурации и API времени выполнения отображаться в отдельных библиотеках DLL методов?</td>
<td>Да. Не забудьте указать различие при настройке записей реестра для самого метода EAP. Пути конфигурации и одноранговых узлов должны указывать на правильные библиотеки DLL.</td>
</tr>
<tr class="even">
<td>Разделы справки установить метод EAP?</td>
<td>Чтобы установить метод EAP, сначала необходимо реализовать [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllRegisterServer) и [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllUnregisterServer) в самой библиотеке DLL метода EAP. После этого используйте <strong>regsvr32.exe</strong> , чтобы установить и удалить метод. Необходимо также задать соответствующие разделы реестра. Дополнительные сведения см. в разделе [Установка метода EAP](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>Что такое поддержка [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP) в аппаратном уровне?</td>
<td>Если включена поддержка NAP в аппаратном контроллере, пакеты NAP передаются внутри пакетов методов EAP. В противоположность этому, если включена поддержка нестандартного NAP, Обмен данными [о состоянии работоспособности](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) NAP выполняется через средства, отличные от внутренних для пакетов методов EAP, а сертификаты, созданные NAP, используются в проверке подлинности методом EAP.</td>
</tr>
<tr class="even">
<td>Можно ли включить поддержку аппаратного контроллера управления NAP для моего метода EAP?</td>
<td>Да, можно включить поддержку аппаратного контроллера управления мобильными NAP для метода EAP. Дополнительные сведения см. в разделе [Включение поддержки NAP In-Band для методов EAP](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>Как работает гибкая Проверка подлинности EAP через безопасное туннелирование (EAP-FAST)?</td>
<td>Сценарий EAP-FAST работает следующим образом. <br/>
<ul>
<li>Метод обрабатывает изменение пароля при едином входе (SSO), использующем пользовательский интерфейс метода.</li>
<li>Метод возвращает атрибут [<strong>еаткредентиалсчанжед</strong>] (/Виндовс/десктоп/АПИ/еаптипес/не-еаптипес-eap_attribute_type).</li>
<li>Сторона сообщает пользователю, что изменились учетные данные, и запрашивает у пользователя повторный ввод учетных данных.</li>
<li>Запрашивающий объект повторно вводит учетные данные пользователя и отправляет эти учетные данные методу.</li>
</ul>
Дополнительные сведения о EAP-FAST см. в статье [гибкая Проверка подлинности EAP с помощью безопасного туннелирования](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-FAST).</td>
</tr>
<tr class="even">
<td>Общие сведения о предварительном ключе (PSK)</td>
<td>Метод передачи и получения цифровых сигналов, в которых фаза передаваемого сигнала изменяется для передачи информации. Поле ввода [<strong>еапконфигинпутпск</strong>] (/Виндовс/десктоп/АПИ/еаптипес/не-еаптипес-eap_config_input_field_type) содержит EAP-FAST PSK пользователя.</td>
</tr>
<tr class="odd">
<td>Что такое WOW и как это имеет значение EAPHost?</td>
<td>Microsoft Windows-32-bit-on-Windows-64-bit (WOW) — это компонент операционной системы в 64-разрядной версии Windows, поддерживающей 32-разрядное приложение платформы x86. Как правило, автор метода EAP определяет определенную форму структуры C/C++, которая позволяет инкапсулировать данные конфигурации, данные учетных данных и интерактивные данные пользовательского интерфейса. Чтобы избежать несовместимости в WOW и других сценариях, важно обеспечить согласованность структур данных в разных архитектурах процессора (32-разрядных и 64-разрядных процессорах). Обычно фиктивное заполнение используется для согласования полей, чтобы параметры конфигурации, учетных данных и интерактивных пользовательских интерфейсов совпадали с 32-и 64-разрядными процессорами.</td>
</tr>
<tr class="even">
<td>Что такое &quot; коды действий &quot; и в каких условиях эти коды действий возвращены?</td>
<td>&quot;Коды действий &quot; позволяют методам управлять потоком проверки подлинности и являются неотъемлемой частью конечного автомата. Это значения, возвращаемые методом EAP для указания следующего действия, которое должна предпринять EAPHost. Например, код действия может указывать на EAPHost, что метод EAP имеет пакет, готовый к передаче. Этот объект придерживается всех кодов действий, возвращаемых методом EAP, но никогда не выдает коды действий. Дополнительные сведения см. в разделе [коды действий для запрашивающих сторон EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактиондискард</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактиондискард</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP для указания EAPHost на то, что он должен отбросить пакет, переданный в метод. В частности, метод определил, что пакет является недопустимым. Затем EAPHost ждет следующего пакета.</td>
</tr>
<tr class="even">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактионсенд</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактионсенд</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP, чтобы указать EAPHost на то, что следующий пакет, полученный с помощью EAPHost, должен быть отправлен на сервер доступа к сети (NAS).</td>
</tr>
<tr class="odd">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактионресулт</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактионресулт</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP, указывающим на EAPHost, что сеанс проверки подлинности закончился и что результаты этого сеанса доступны.</td>
</tr>
<tr class="even">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактионинвокеуи</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактионинвокеуи</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP, чтобы указать EAPHost на то, что для продолжения проверки подлинности требуются входные данные пользователя, и для получения этих входных данных необходимо диалоговое окно пользовательского интерфейса. После получения данных, вводимых пользователем, EAPHost может снова вызвать метод EAP с обновленными данными контекста пользовательского интерфейса.</td>
</tr>
<tr class="odd">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактионреспонд</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактионреспонд</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP, чтобы указать EAPHost на то, что метод EAP имеет атрибуты, доступные для использования EAPHost во время проверки подлинности. EAPHost получает атрибуты путем вызова метода [<strong>еаппиржетреспонсеаттрибутес</strong>] (/превиаус-версионс/Виндовс/десктоп/АПИ/еапмесодпирапис/НФ-еапмесодпирапис-еаппиржетреспонсеаттрибутес), за которым следует вызов метода [<strong>EapPeerSetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes).</td>
</tr>
<tr class="even">
<td>Когда метод возвращает [<strong>еаппирмесодреспонсеактионноне</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) и что означает, что этот код действия имеет значение EAPHost?</td>
<td>[<strong>Еаппирмесодреспонсеактионноне</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/Ne-eapauthenticatoractiondefine-eappeermethodresponseaction) возвращается методом EAP, чтобы указать EAPHost на то, что в настоящее время никаких действий не требуется.</td>
</tr>
<tr class="odd">
<td>Можно ли включить трассировку на стороне средства проверки подлинности?</td>
<td>Да. Дополнительные сведения см. в разделе [Включение трассировки](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по API однорангового метода EAPHost](eap-host-peer-method-api-reference.md)
</dt> <dt>

[Общие вопросы и ответы по EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Вопросы и ответы по обращению EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Вопросы и ответы по разработке EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

