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
ms.openlocfilehash: 501f98ec1b360e3eaa10988c140f30b86dcacb5a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987347"
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


| Метка | Применение |
|--------|-------|
| <p>Значение по умолчанию:</p> | <p>Значение параметра по умолчанию.</p> | 
| <p>Тип:</p> | <p>Тип данных параметра.</p> | 
| <p>Допустимый диапазон:</p> | <p>Допустимые значения для параметра.</p> | 
| <p>Область.</p> | <p>Является ли параметр глобальным или для каждого экземпляра?</p> | 
| <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Можно ли задать параметр, если существуют какие бы то ни было экземпляры?</p> | 
| <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Можно ли задать параметр при инициализации?</p> | 
| <p>Влияет на физический макет:</p> | <p>Влияет ли параметр на файлы на диске?</p> | 
| <p>Влияет на надежность:</p> | <p>Влияет ли параметр на надежность ядра?</p> | 
| <p>Влияет на производительность:</p> | <p>Влияет ли параметр на производительность ядра?</p> | 
| <p>Влияет на ресурсы:</p> | <p>Влияет ли параметр на ресурсы ядра?</p> | 
| <p>"Доступность":</p> | <p>выпуски Windows, которые поддерживают параметр.</p> | 

