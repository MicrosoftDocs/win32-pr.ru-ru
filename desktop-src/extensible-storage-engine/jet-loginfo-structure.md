---
description: 'Дополнительные сведения: структура JET_LOGINFO'
title: Структура JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983167"
---
# <a name="jet_loginfo-structure"></a>Структура JET_LOGINFO


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_loginfo-structure"></a>Структура JET_LOGINFO

Структура **JET_LOGINFO** возвращает структурированную информацию о наборе файлов журналов транзакций, которые должны быть частью набора файлов резервной копии. Структура **JET_LOGINFO** — это минимальный набор сведений, необходимых для представления диапазона журналов, получаемых с помощью [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) или указанных для жесткого восстановления с помощью [JetExternalRestore2](./jetexternalrestore2-function.md).

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Элементы

**кбсизе**

Размер структуры в байтах.

Этот член обеспечивает будущее расширение этой структуры, одновременно обеспечивая обратную совместимость. Для него всегда должно быть задано значение sizeof (JET_LOGINFO).

**улженлов**

Самый низкий (или самый старый) номер файла журнала, который восстанавливается. Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF. Это может измениться в будущих версиях.

**улженхигх**

Самый высокий (или самый последний) номер файла журнала, который восстанавливается. Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF. Это может измениться в будущих версиях.

**сзбасенаме**

Префикс, используемый для именования файлов журнала транзакций.

Значение, возвращаемое в этом элементе, всегда равно значению параметра [JET_paramBaseName](./transaction-log-parameters.md) для экземпляра, который создал эти сведения.

### <a name="remarks"></a>Комментарии

Имена файлов журналов транзакций задаются в соответствии с базовым именем экземпляра и номером поколения файла журнала. Имя имеет формат БББКСКСКСКСКС. Журналь. BBB соответствует базовому имени файла журнала и всегда имеет три символа. XXXXX соответствует номеру поколения файла журнала в шестнадцатеричном формате без дополнения и всегда имеет длину пять символов. LOG — это расширение файла, которое всегда передается в файлы журнала транзакций ядром.

Использование этой структурированной информации не рекомендуется, так как оно заставляет приложение иметь глубокую информацию о схеме именования для файлов журнала транзакций. Если схема именования когда-либо изменится в будущем, это приложение перестанет работать правильно. Это представить, что формат журнала изменится на включение 8 шестнадцатеричных цифр в будущем. Приложения должны использовать явный список имен файлов, возвращаемых функцией [жетжетлогинфо](./jetgetloginfo-function.md) .

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_LOGINFO_W</strong> (Юникод) и <strong>JET_LOGINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[жетжетлогинфо](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
