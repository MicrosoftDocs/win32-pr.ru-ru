---
description: 'Дополнительные сведения: структура JET_INDEXID'
title: Структура JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712881"
---
# <a name="jet_indexid-structure"></a>Структура JET_INDEXID

Содержит идентификатор индекса. Идентификатор индекса — это указание, которое используется для ускорения выбора текущего индекса с помощью Жетсеткуррентиндекс. Это наиболее полезно при наличии очень большого количества индексов в таблице. Идентификатор индекса можно получить с помощью Жетжетиндексинфо или Жетжеттаблеиндексинфо.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a>Примечания

Атрибут Pack необходим, так как версия C++ определена как массив байтов. Если компилятор C \# вставляет обычное заполнение между uint кбструкт и IntPtr, структура заканчивается слишком большим.

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы JET_INDEXID](./jet-indexid-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
