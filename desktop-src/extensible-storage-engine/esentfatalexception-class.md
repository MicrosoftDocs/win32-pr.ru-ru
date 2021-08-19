---
description: 'Дополнительные сведения о: Есентфаталексцептион Class'
title: Класс EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53e5653d33dfd586ca5a066231f512c83684f3ea6ba53de74c0d3cb29cc4dbb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118496743"
---
# <a name="esentfatalexception-class"></a>Класс EsentFatalException

Базовый класс для неустранимых исключений.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентфаталексцептион](./esentfatalexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентинстанцеунаваилабледуетофаталлогдискфуллексцептион](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинстанцеунаваилабликсцептион](./esentinstanceunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогдисабледдуеторековерифаилуриксцептион](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентроллбаккеррорексцептион](./esentrollbackerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсекторсизенотсуппортедексцептион](./esentsectorsizenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентунлоадаблеосфунктионалитексцептион](./esentunloadableosfunctionalityexception-class.md)