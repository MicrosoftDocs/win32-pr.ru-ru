---
description: 'Дополнительные сведения о методе: Server2003Api. JetUpdate2'
title: Server2003Api. JetUpdate2, метод (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f19d0bb4ab599e2f7a11ac66202c805066c1744b80ed72223d20be423340d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978574"
---
# <a name="server2003apijetupdate2-method"></a>Server2003Api. JetUpdate2, метод

Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки. Удаление строки таблицы выполняется путем вызова [жетделете (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, который запустил обновление.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Обновляемый курсор. Необходимо подготовить обновление.

<!-- end list -->

  - закладка  
    Тип \[\]  
    
    Возвращает закладку обновленной записи. Может принимать значение NULL.

<!-- end list -->

  - букмарксизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер буфера закладок.

<!-- end list -->

  - актуалбукмарксизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает фактический размер закладки.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. server2003. упдатегрбит](./updategrbit-enumeration.md)  
    
    Параметры обновления.

## <a name="remarks"></a>Remarks

Жетупдате является последним шагом в выполнении вставки или обновления. Обновление начинается с вызова [жетпрепареупдате (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , а затем путем вызова [жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, сетколумнгрбит, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) один или несколько раз для задания состояния записи. Наконец, \[ \] для завершения операции обновления вызывается JetUpdate2 (JET_SESID, JET_TABLEID,, Int32, Int32, упдатегрбит). Индексы обновляются только в Жетупдате или, а не во время Жетсетколумн.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс Server2003Api](./server2003api-class.md)

[Элементы Server2003Api](./server2003api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
