---
description: Дополнительные сведения о методе API. JetDefragment2
title: API. JetDefragment2, метод
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710954"
---
# <a name="apijetdefragment2-method"></a>API. JetDefragment2, метод

Запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, используемый для вызова.

<!-- end list -->

  - dbid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Дефрагментированная база данных.

<!-- end list -->

  - tableName  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Неиспользуемый параметр. Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.

<!-- end list -->

  - соответствующий  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное число проходов дефрагментации. При остановке задачи дефрагментации в оперативном режиме для этого параметра задается количество выполненных проходов.

<!-- end list -->

  - секунд  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное время для дефрагментации. При остановке задачи дефрагментации в оперативном режиме этот выходной буфер задается в течение времени, используемого для дефрагментации.

<!-- end list -->

  - обратный вызов  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Функция обратного вызова, используемая для отчета о ходе выполнения в дефрагментации.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. дефраггрбит](./defraggrbit-enumeration.md)  
    
    Параметры дефрагментации.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Код предупреждения.  

## <a name="remarks"></a>Комментарии

Обратный вызов, передаваемый в JetDefragment2, может выполняться асинхронно. Сборщик мусора не знает, что неуправляемый код имеет ссылку на обратный вызов, поэтому важно убедиться, что обратный вызов не собирается.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
