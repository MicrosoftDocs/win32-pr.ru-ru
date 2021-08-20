---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. пидксуникоде'
title: Свойство JET_OPENTEMPORARYTABLE. пидксуникоде (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 378c1497d57e3d904398d92d654579cc4a8702271db3525a2943e50ae3d03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118074028"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>Свойство JET_OPENTEMPORARYTABLE. пидксуникоде

Возвращает или задает код локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице. Если этот параметр имеет значение null, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию. По умолчанию используется языковой стандарт «Английский (США)». Если этот параметр имеет значение null, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию. Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Элементы JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
