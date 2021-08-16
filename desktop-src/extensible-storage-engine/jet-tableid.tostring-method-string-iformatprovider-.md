---
description: 'Дополнительные сведения о: JET_TABLEID. Метод ToString (String, IFormatProvider)'
title: JET_TABLEID. Метод ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a674e980f86b57e7dd12fe451bc413b5b9b2f90b4cdc218be8753d7955376997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979204"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a>JET_TABLEID. Метод ToString (String, IFormatProvider)

Форматирует значение текущего экземпляра, используя указанный формат.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Параметры

  - format  
    Тип: [System. String](/dotnet/api/system.string)  
    
    [Строка](/dotnet/api/system.string) , указывающая используемый формат. или значение null, чтобы использовать формат по умолчанию, определенный для типа реализации [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - formatProvider  
    Тип: [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider](/dotnet/api/system.iformatprovider) , используемый для форматирования значения; или значение NULL для получения сведений о форматировании чисел из текущего параметра языкового стандарта операционной системы.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. String](/dotnet/api/system.string)  
[Строка](/dotnet/api/system.string) , содержащая значение текущего экземпляра в указанном формате.  

#### <a name="implements"></a>Реализации

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_TABLEID](./jet-tableid-structure.md)

[Элементы JET_TABLEID](./jet-tableid-members.md)

[Перегрузка ToString](./jet-tableid.tostring-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
