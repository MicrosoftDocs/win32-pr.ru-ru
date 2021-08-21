---
description: 'Дополнительные сведения о: Есентстатиксцептион Class'
title: Класс EsentStateException
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125680795e7cb1bda2a63dd871ef02bf4595970ba774fa74a72490de628f1b5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064054"
---
# <a name="esentstateexception-class"></a>Класс EsentStateException

Базовый класс для исключений состояния.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентстатиксцептион](./esentstateexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентбаккупинпрогрессексцептион](./esentbackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбаккупноталловедетексцептион](./esentbackupnotallowedyetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадитагсекуенцеексцептион](./esentbaditagsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбуффертусмаллексцептион](./esentbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткаллбаккфаиледексцептион](./esentcallbackfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеалреадюпградедексцептион](./esentdatabasealreadyupgradedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасефаилединкременталресидексцептион](./esentdatabasefailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеупградиксцептион](./esentdatabaseincompleteupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабаселеакинспацеексцептион](./esentdatabaseleakinspaceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдиртишутдовнексцептион](./esentdirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфиленотфаундексцептион](./esentfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентиндексинусиксцептион](./esentindexinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентиндекснотфаундексцептион](./esentindexnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидбуфферсизиксцептион](./esentinvalidbuffersizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидлогдатасекуенцеексцептион](./esentinvalidlogdatasequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткэйдупликатиксцептион](./esentkeyduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткэйтрункатедексцептион](./esentkeytruncatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогфилесиземисматчдатабасесконсистентексцептион](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогсекторсиземисматчдатабасесконсистентексцептион](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлснотсетексцептион](./esentlsnotsetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингфуллбаккупексцептион](./esentmissingfullbackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмултивалуеддупликатеафтертрункатионексцептион](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмултивалуеддупликатиксцептион](./esentmultivaluedduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентноаттачментсфаилединкременталресидексцептион](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентнобаккупексцептион](./esentnobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентнокуррентрекордексцептион](./esentnocurrentrecordexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентобжектнотфаундексцептион](./esentobjectnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентосснапшотноталловедексцептион](./esentossnapshotnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекордделетедексцептион](./esentrecorddeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекорднотфаундексцептион](./esentrecordnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекордтубижексцептион](./esentrecordtoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекордтубигфорбакквардкомпатибилитексцептион](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрековередвисеррорсексцептион](./esentrecoveredwitherrorsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрековередвисаутундодатабасесконсистентексцептион](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрековередвисаутундоексцептион](./esentrecoveredwithoutundoexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрестореинпрогрессексцептион](./esentrestoreinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсепаратедлонгвалуиксцептион](./esentseparatedlongvalueexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсуррогатебаккупинпрогрессексцептион](./esentsurrogatebackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттабледупликатиксцептион](./esenttableduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттаблеинусиксцептион](./esenttableinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттестинжектионнотсуппортедексцептион](./esenttestinjectionnotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентвритеконфликтексцептион](./esentwriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентвритеконфликтпримариндексексцептион](./esentwriteconflictprimaryindexexception-class.md)