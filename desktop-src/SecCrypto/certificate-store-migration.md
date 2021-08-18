---
description: При обновлении компьютера или переносе компьютера на компьютер будут перенесены сертификаты в определенных хранилищах сертификатов.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Перенос хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771100"
---
# <a name="certificate-store-migration"></a>Перенос хранилища сертификатов

При обновлении компьютера или переносе компьютера на компьютер будут перенесены сертификаты в определенных хранилищах сертификатов. В следующей таблице перечислены хранилища сертификатов, которые переносятся по умолчанию. для хранилища Параметры автоматического запроса сертификатов (записи контроля доступа) переносятся только [*списки доверия сертификатов*](../secgloss/c-gly.md) (ctl). Для всех остальных магазинов, перечисленных ниже, переносятся только сертификаты.

<table>
<thead>
<tr class="header">
<th>Система или пользователь</th>
<th>Хранение</th>
<th>Расположение хранения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {Remove} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Корневая папка</strong> \ <strong>Сертификаты</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Мой</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрос</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Трустедпублишер</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>TrustedPeople</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="even">
<td>Запрещено</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрещено</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="odd">
<td>Целостности и доступности</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Центр сертификации</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="even">
<td>ЗАПИСИ контроля доступа</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Записи контроля доступа</strong> \ <strong>Списки CTL</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Пользователь $ {Remove} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Корневая папка</strong> \ <strong>Сертификаты</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>файл: \\ %аппдата%\микрософт\системцертификатес\ми\цертификатес</td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td>файл: \\ %аппдата%\микрософт\системцертификатес\рекуест\цертификатес</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Трустедпублишер</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>TrustedPeople</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="even">
<td>Запрещено</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрещено</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
<tr class="odd">
<td>Целостности и доступности</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Центр сертификации</strong> \ <strong>Сертификаты</strong><br/></td>

</tr>
</tbody>
</table>



 

Другие хранилища сертификатов, созданные приложениями, не переносятся по умолчанию. Приложения, которые создают собственные магазины, отвечают за миграцию созданных ими магазинов. Для создания магазинов рекомендуется определить раздел реестра в параметрах приложения и создать хранилище в параметрах реестра с помощью поставщика **\_ хранилища сертификатов \_ Prov \_ reg** Store. Дополнительные сведения о переносе параметров приложения см. в разделе *Создание пользовательского .xml файла* статьи Руководство по *использованию средства USMT 3,0* по адресу [средство миграции пользовательской среды 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Этот ресурс может быть недоступен в некоторых языках и странах или регионах.)

 

 
