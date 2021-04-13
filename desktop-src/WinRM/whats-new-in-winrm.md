---
title: Новые возможности WinRM 2,0
description: Новые возможности доступны в служба удаленного управления Windows версии 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412607"
---
# <a name="whats-new-in-winrm-20"></a>Новые возможности WinRM 2,0

Новые возможности доступны в служба удаленного управления Windows версии 2,0. (WinRM 2,0)

WinRM 2,0 входит в Windows Server 2008 R2 и Windows 7.

Кроме того, можно загрузить WinRM 2,0 для Windows Server 2008 с пакетом обновления 2 (SP2) и Windows Vista с пакетом обновления 2 (SP2). Сведения о скачивании WinRM 2,0 см. в разделе [KB968929](https://support.microsoft.com/kb/968929).

В следующей таблице приведена документация по WinRM 2,0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">API оболочки клиента WinRM</a><br/></td>
<td>Интерфейс прикладного программирования (API) оболочки клиента WinRM предоставляет функциональные возможности для создания оболочек, команд и потоков данных на удаленных компьютерах и управления ими. <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">API подключаемого модуля WinRM</a><br/></td>
<td>Интерфейс API подключаемого модуля WinRM предоставляет функциональные возможности, позволяющие пользователю создавать подключаемые модули, реализуя определенные API для поддерживаемых URI и операций с <a href="windows-remote-management-glossary.md"><em>ресурсами</em></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">Инфраструктура для управления размещенными службами</a><br/></td>
<td>В WinRM 2,0 введена платформа размещения. Поддерживаются две модели размещения. Одна из них — служба IIS, а другая — WinRM — на основе службы. <br/> Дополнительные сведения о конфигурации узла см. в следующих разделах:<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">Конфигурация подключаемого модуля узла IIS</a></li>
<li><a href="wsman-service-plug-in-configuration.md">Конфигурация подключаемого модуля службы WinRM</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">Обнаружение профиля DMTF с помощью обхода взаимосвязей</a><br/></td>
<td>Обход ассоциации позволяет пользователю извлекать экземпляры классов взаимосвязей с помощью стандартного механизма фильтрации.<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">Усовершенствования инфраструктуры удаленной оболочки</a><br/></td>
<td>Этот раздел содержит сведения об улучшениях удаленной инфраструктуры для WinRM. <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">Поддержка нескольких прыжков</a><br/></td>
<td>В WinRM 2,0 добавлена функция, которая поддерживает делегирование учетных данных пользователя на нескольких удаленных компьютерах. <br/> В разделе <a href="authentication-constants.md"><strong>константы проверки подлинности</strong></a> добавлена следующая константа: <strong>всманфлагусекредссп</strong>.<br/> Следующий API C++ был добавлен для обеспечения поддержки нескольких прыжков: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br/> Добавлен следующий API скриптов для обеспечения поддержки нескольких прыжков: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. сессионфлагусекредссп</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">Управление квотами для удаленных оболочек</a><br/></td>
<td>В этом разделе содержатся сведения о настройке квот для управления удаленной оболочкой.<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">Управляемый Справочник по командам PowerShell WS-Management</a><br/></td>
<td>Пользователи WinRM 2,0 могут использовать командлеты Windows PowerShell для управления системой.<br/></td>
</tr>
</tbody>
</table>



 

 

 





