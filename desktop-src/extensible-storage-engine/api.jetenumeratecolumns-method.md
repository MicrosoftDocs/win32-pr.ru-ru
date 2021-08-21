---
description: Дополнительные сведения о методе API. Жетенумератеколумнс
title: API. Жетенумератеколумнс, метод
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 713b02835aa063e888a2385df9bd8abdff9af1300a2e9885c06e995f2b814bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042712"
---
# <a name="apijetenumeratecolumns-method"></a>API. Жетенумератеколумнс, метод

Эффективно извлекает набор столбцов и их значений из текущей записи курсора или буфера копирования этого курсора. Возвращаемые столбцы и значения могут быть ограничены списком идентификаторов столбцов, Итагсекуенце числами и другими характеристиками. Этот интерфейс API извлечения столбца уникален в том, что он возвращает сведения в динамически выделяемой памяти, получаемой с помощью предоставленного пользователем обратного вызова, совместимого с переопределением. Эта новая гибкость позволяет эффективно получать данные столбцов с определенными характеристиками (например, размер и количество элементов), неизвестных вызывающему объекту. Это устраняет необходимость использования режимов обнаружения Жетретриевеколумн для определения этих характеристик, чтобы настроить окончательный вызов Жетретриевеколумн, который будет успешно получать нужные данные.

Этот API несовместим с CLS. 

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, из которого извлекаются данные.

<!-- end list -->

  - нумколумнидс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число JET_ENUMCOLUMNIDS.

<!-- end list -->

  - колумнидс  
    Тип \[\]  
    
    Необязательный массив идентификаторов столбцов, каждый из которых имеет необязательный массив чисел Итагсекуенце для перечисления.

<!-- end list -->

  - нумколумнвалуес  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает число извлеченных значений столбцов.

<!-- end list -->

  - колумнвалуес  
    Тип \[\]  
    
    Возвращает перечисляемые значения столбцов.

<!-- end list -->

  - allocator  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Обратный вызов, используемый для выделения памяти.

<!-- end list -->

  - аллокаторконтекст  
    Тип: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Контекст для обратного вызова выделения.

<!-- end list -->

  - максдатасизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Устанавливает ограничение на объем данных, возвращаемых из длинного текстового или длинного двоичного столбца. Этот параметр можно использовать, чтобы предотвратить перечисление слишком большого значения столбца.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. енумератеколумнсгрбит](./enumeratecolumnsgrbit-enumeration.md)  
    
    Получение параметров.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Предупреждение или успешное завершение.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
