---
description: 'Дополнительные сведения о: Есентоператионексцептион Class'
title: Класс EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105713237"
---
# <a name="esentoperationexception-class"></a>Класс EsentOperationException

Базовый класс для исключений операций.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион  
          

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентоператионексцептион](./esentoperationexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион  
          [Microsoft. ISAM. ESENT. Interop. Есентбаккупабортбисерверексцептион](./esentbackupabortbyserverexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентчеккпоинтдепстудипексцептион](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентклиентрекуесттостопжетсервицеексцептион](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион](./esentfatalexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентинитинпрогрессексцептион](./esentinitinprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентинтерналеррорексцептион](./esentinternalerrorexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентиоексцептион](./esentioexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентнтсистемкаллфаиледексцептион](./esentntsystemcallfailedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентосснапшоттимеаутексцептион](./esentossnapshottimeoutexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентрекорднотделетедексцептион](./esentrecordnotdeletedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион](./esentresourceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есенттерминпрогрессексцептион](./esentterminprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентуникоделангуажевалидатионфаилуриксцептион](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентуникодетранслатионфаилексцептион](./esentunicodetranslationfailexception-class.md)