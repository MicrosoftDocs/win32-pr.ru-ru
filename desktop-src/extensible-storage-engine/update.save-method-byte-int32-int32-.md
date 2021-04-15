---
description: Дополнительные сведения см. в статье метод обновления. Save (Byte, Int32, Int32).
title: Метод Update. Save (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497619"
---
# <a name="updatesave-method-byte--int32-int32"></a>Метод Update. Save (Byte, Int32, Int32)

Обновите TableID.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Параметры

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

## <a name="remarks"></a>Комментарии

Сохранение является последним шагом в выполнении вставки или обновления. Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи. Наконец, для завершения операции обновления вызывается обновление. Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс обновления](./update-class.md)

[Обновить элементы](./update-members.md)

[Сохранить перегрузку](./update.save-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
