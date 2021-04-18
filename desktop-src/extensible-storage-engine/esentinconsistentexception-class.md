---
description: 'Дополнительные сведения о: Есентинконсистентексцептион Class'
title: Класс EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105674525"
---
# <a name="esentinconsistentexception-class"></a>Класс EsentInconsistentException

Базовый класс для непоследовательных исключений.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентинконсистентексцептион](./esentinconsistentexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентаттачеддатабасемисматчексцептион](./esentattacheddatabasemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадчеккпоинтсигнатуриксцептион](./esentbadcheckpointsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадлогсигнатуриксцептион](./esentbadlogsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадлогверсионексцептион](./esentbadlogversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентчеккпоинтфиленотфаундексцептион](./esentcheckpointfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентконсистенттимемисматчексцептион](./esentconsistenttimemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабаседиртишутдовнексцептион](./esentdatabasedirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеинкременталресидексцептион](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабаселогсетмисматчексцептион](./esentdatabaselogsetmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдбтиметуневексцептион](./esentdbtimetoonewexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдбтиметуолдексцептион](./esentdbtimetoooldexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентендингресторелогтуловексцептион](./esentendingrestorelogtoolowexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентексистинглогфилехасбадсигнатуриксцептион](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентексистинглогфилеиснотконтигуаусексцептион](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеинвалидтипиксцептион](./esentfileinvalidtypeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентгивенлогфилехасбадсигнатуриксцептион](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентгивенлогфилеиснотконтигуаусексцептион](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидкреатедбверсионексцептион](./esentinvalidcreatedbversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалиддатабасеверсионексцептион](./esentinvaliddatabaseversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогженератионмисматчексцептион](./esentloggenerationmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингкуррентлогфилесексцептион](./esentmissingcurrentlogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингфилетобаккупексцептион](./esentmissingfiletobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингресторелогфилесексцептион](./esentmissingrestorelogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентпажесиземисматчексцептион](./esentpagesizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекуиредлогфилесмиссинжексцептион](./esentrequiredlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентстартингресторелогтухигхексцептион](./esentstartingrestorelogtoohighexception-class.md)