---
description: Дополнительные сведения о методе API. Жетготосекондариндексбукмарк
title: API. Жетготосекондариндексбукмарк, метод
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93d85897f81e27cc1e5704bd5524adf4abd921e86e9d5ad24f5893ee4384c427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455724"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a>API. Жетготосекондариндексбукмарк, метод

Позиционирует курсор на запись индекса, связанную с закладкой дополнительного индекса. Закладку вторичного индекса необходимо использовать с тем же индексом для той же таблицы, из которой она была первоначально извлечена. Закладку вторичного индекса для записи индекса можно получить с помощью Жетготосекондариндексбукмарк (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, готосекондариндексбукмаркгрбит).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор таблицы для позиционирования.

<!-- end list -->

  - secondaryKey  
    Тип \[\]  
    
    Буфер, содержащий вторичный ключ.

<!-- end list -->

  - секондарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер вторичного ключа.

<!-- end list -->

  - primaryKey  
    Тип \[\]  
    
    Буфер, содержащий первичный ключ.

<!-- end list -->

  - примарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер первичного ключа.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. готосекондариндексбукмаркгрбит](./gotosecondaryindexbookmarkgrbit-enumeration.md)  
    
    Параметры для размещения закладки.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
