---
description: Дополнительные сведения о методе API. Жеткомпакт
title: API. Жеткомпакт, метод
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990997"
---
# <a name="apijetcompact-method"></a>API. Жеткомпакт, метод

Создает копию существующей базы данных. Копия сжимается в состояние, оптимальное для использования. Данные в скопированных данных будут упаковываться в соответствии с мерами, выбранными для индексов при создании индекса. Таким образом, сжатые данные могут храниться как можно более плотно. Кроме того, сжатые данные могут резервировать пространство для последующего роста записи или вставки индекса.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, используемый для вызова.

<!-- end list -->

  - sourceDatabase  
    Тип: [System. String](/dotnet/api/system.string)  
    
    База данных источника, которая будет сжата.

<!-- end list -->

  - destinationDatabase  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя, используемое для сжатой базы данных.

<!-- end list -->

  - статускаллбакк  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Функция обратного вызова, которую можно периодически вызывать с помощью операции Database Compact для отчета о ходе выполнения.

<!-- end list -->

  - не учитывается  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Этот параметр игнорируется и должен иметь значение null.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. компактгрбит](./compactgrbit-enumeration.md)  
    
    Параметры сжатия.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
