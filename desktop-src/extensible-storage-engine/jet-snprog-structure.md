---
description: 'Дополнительные сведения: структура JET_SNPROG'
title: Структура JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
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
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987737"
---
# <a name="jet_snprog-structure"></a>Структура JET_SNPROG


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_snprog-structure"></a>Структура JET_SNPROG

Структура **JET_SNPROG** содержит сведения о ходе выполнения длительной операции. Когда вызывается функция обратного вызова для уведомления о состоянии операции, и операция все еще выполняется, последний параметр функции обратного вызова является указателем на структуру **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры **JET_SNPROG** в байтах. Это значение подтверждает наличие следующих полей.

**кунитдоне**

Количество рабочих единиц, уже выполненных во время выполнения длительной функции.

**куниттотал**

Количество единиц работы, которые необходимо выполнить. Это значение всегда должно быть больше или равно **кунитдоне**.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


