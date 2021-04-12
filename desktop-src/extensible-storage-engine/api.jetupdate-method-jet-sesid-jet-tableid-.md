---
description: 'Дополнительные сведения: метод API. Жетупдате (JET_SESID, JET_TABLEID)'
title: Метод API. Жетупдате (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349585"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a>Метод API. Жетупдате (JET_SESID, JET_TABLEID)

Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки. Удаление строки таблицы выполняется путем вызова [жетделете (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
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

## <a name="remarks"></a>Комментарии

Жетупдате является последним шагом в выполнении вставки или обновления. Обновление начинается с вызова [жетпрепареупдате (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , а затем путем вызова [жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, сетколумнгрбит, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) один или несколько раз для задания состояния записи. Наконец, для завершения операции обновления вызывается [жетупдате (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) . Индексы обновляются только в Жетупдате или, а не во время Жетсетколумн.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жетупдате](./api.jetupdate-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
