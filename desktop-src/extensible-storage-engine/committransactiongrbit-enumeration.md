---
description: Дополнительные сведения о перечислении Коммиттрансактионгрбит
title: Перечисление Коммиттрансактионгрбит
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: efe052fc01014d3ebb624dbd4183bc8f0584b145
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481790"
---
# <a name="committransactiongrbit-enumeration"></a>Перечисление Коммиттрансактионгрбит

Параметры для Жеткоммиттрансактион.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a>Члены


|  | Имя участника | Описание | 
|--|-------------|-------------|
|  | None | Параметры по умолчанию. | 
|  | лазифлуш | Транзакция фиксируется обычным образом, но этот API не ждет сброса транзакции в файл журнала транзакций перед возвратом вызывающему объекту. Это радикально сокращает продолжительность операции фиксации за счет устойчивости. Любая транзакция, которая не сброшена в журнал до сбоя, будет автоматически прервана во время восстановления после сбоя во время следующего вызова Жетинит. Если указаны WaitLastLevel0Commit или WaitAllLevel0Commit, этот параметр не учитывается. | 
|  | WaitLastLevel0Commit | Если в сеансе ранее зафиксированы транзакции и они еще не были записаны в файл журнала транзакций, они должны быть сброшены немедленно. Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект. Это полезно, если приложение ранее зафиксировало несколько транзакций с помощью JET_bitCommitLazyFlush и теперь хочет сбросить все эти транзакции на диск.<p>Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции. Этот параметр нельзя использовать в сочетании с любым другим параметром.</p> | 



## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
