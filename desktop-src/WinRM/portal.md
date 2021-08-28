---
title: Удаленное управление Windows
description: Windows удаленное управление (служба удаленного управления Windows) — это реализация WS-Management протокола майкрософт стандартного протокола на основе SOAP, обеспечивающего взаимодействие оборудования и операционных систем от разных поставщиков.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Удаленное управление (WinRM), начальная страница
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c816e3f7092fc7825407497793ed529df13cf9115426b63e4b535bd019f81df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858764"
---
# <a name="windows-remote-management"></a>Удаленное управление Windows

## <a name="purpose"></a>Назначение

С помощью удаленного управления Windows (WinRM) корпорация Майкрософт реализует стандартный [протокол WS-Management](ws-management-protocol.md), основанный на протоколе SOAP. Он удобен для брандмауэров и обеспечивает взаимодействие оборудования и операционных систем различных поставщиков.

Спецификация протокола WS-Management предоставляет системам общий способ доступа и обмена данными управления в ИТ-инфраструктуре. WinRM и [*интеллектуальный интерфейс управления платформой (IPMI)*](windows-remote-management-glossary.md)вместе с [сборщиком событий](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) являются компонентами компонентов [Windows аппаратного управления](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .

## <a name="where-applicable"></a>Где применимо

для получения данных управления с локальных и удаленных компьютеров, на которых могут использоваться [*контроллеры управления основной платой (bmc)*](windows-remote-management-glossary.md), можно использовать объекты скриптов winrm, программу командной строки winrm или средство командной строки Windows удаленной оболочки. если компьютер работает под управлением Windows версии операционной системы, включающей WinRM, данные управления передаются [инструментарий управления Windows (WMI) (WMI)](/windows/desktop/WmiSdk/wmi-start-page).

Данные об оборудовании и системе также можно получить из реализаций протокола WS-Management, работающих в других операционных системах (не Windows) на предприятии. WinRM устанавливает сеанс связи с другим компьютером по протоколу WS-Management на основе SOAP, а не подключается через DCOM, как WMI. Данные возвращаются протоколу WS-Management в формате XML, а не в виде объектов.

Поставщик [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI — это стандартный поставщик WMI с классами, получающими данные датчика BMC с компьютеров с соответствующим оборудованием. Доступ к данным IPMI можно получить с помощью API-интерфейсов WinRM, [скриптов](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI или [com](/windows/desktop/WmiSdk/com-api-for-wmi) .

## <a name="developer-audience"></a>Аудитория разработчиков

аудитория разработчика — это Pro, который пишет сценарии для автоматизации управления серверами или разработчиком ISV, получающим данные для приложений управления.

## <a name="run-time-requirements"></a>Требования к среде выполнения

WinRM является частью операционной системы. Однако для получения данных с удаленных компьютеров необходимо настроить [*прослушиватель*](windows-remote-management-glossary.md#l)WinRM. дополнительные сведения см. в разделе [установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md). Если контроллер BMC обнаруживается при запуске системы, поставщик IPMI загружается; в противном случае объекты скриптов WinRM и средство командной строки WinRM остаются доступными.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[о служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dd>

Ссылка на общедоступную спецификацию протокола WS-Management, архитектуру WinRM, связь с WMI, управление оборудованием с помощью поставщика IPMI, конфигурации и установки.

</dd> <dt>

[использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dd>

Приступая к работе с API-интерфейсом WinRM Scripting и аппаратным управлением.

</dd> <dt>

[Windows Справочник по удаленному управлению](windows-remote-management-reference.md)
</dt> <dd>

Список интерфейсов сценариев, определенных веб-службами Майкрософт для автоматизации управления (WS-Management) и определений классов классов WMI, созданных поставщиком IPMI и классами, взаимодействующими с драйвером IPMI для получения данных [контроллера управления основной платой (BMC)](windows-remote-management-glossary.md) .

</dd> </dl>

 

 