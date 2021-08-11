---
description: 'дополнительные сведения: расширяемые системные параметры служба хранилища Engine'
title: расширяемые параметры системы служба хранилища Engine
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 531e599c66279312f80216f1eb09fc612636821227e76f3572645ab6b4ee5137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256451"
---
# <a name="extensible-storage-engine-system-parameters"></a>расширяемые параметры системы служба хранилища Engine


_**Применимо к:** Windows | Windows Сервером_

## <a name="extensible-storage-engine-system-parameters"></a>расширяемые параметры системы служба хранилища Engine

Следующие константы используются в качестве значений для параметра *парамид* функций [жетжетсистемпараметер](./jetgetsystemparameter-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md) .

  - [Параметры резервного копирования и восстановления](./backup-and-restore-parameters.md)

  - [Параметры обратного вызова](./callback-parameters.md)

  - [Параметры базы данных](./database-parameters.md)

  - [Параметры кэша базы данных](./database-cache-parameters.md)

  - [Параметры обработки ошибок](./error-handling-parameters.md)

  - [Параметры журнала событий](./event-log-parameters.md)

  - [Параметры ввода-вывода](./i-o-parameters.md)

  - [Параметры индекса](./index-parameters.md)

  - [Информационные параметры](./informational-parameters.md)

  - [Параметры Meta](./meta-parameters.md)

  - [Параметры ресурсов](./resource-parameters.md)

  - [Параметры временной базы данных](./temporary-database-parameters.md)

  - [Параметры журнала транзакций](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Формат описания параметров системы

Каждый системный параметр будет описан в следующем формате:

JET_paramX

Описание системного параметра JET_paramX.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Значение параметра по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Тип данных параметра.</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>Допустимые значения для параметра.</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Является ли параметр глобальным или для каждого экземпляра?</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Можно ли задать параметр, если существуют какие бы то ни было экземпляры?</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Можно ли задать параметр при инициализации?</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Влияет ли параметр на файлы на диске?</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Влияет ли параметр на надежность ядра?</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Влияет ли параметр на производительность ядра?</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Влияет ли параметр на ресурсы ядра?</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>выпуски Windows, которые поддерживают параметр.</p></td>
</tr>
</tbody>
</table>
