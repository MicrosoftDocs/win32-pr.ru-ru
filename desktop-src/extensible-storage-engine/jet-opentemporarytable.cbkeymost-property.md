---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. Кбкэймост'
title: Свойство JET_OPENTEMPORARYTABLE. Кбкэймост (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 225c801770bb41337ee9f3ae248092c60441cd2e9a059f64897ad19053bfe30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107703"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>Свойство JET_OPENTEMPORARYTABLE. Кбкэймост

Возвращает или задает максимальный размер ключа, представляющего заданную строку. Для управления способом усечения ключей можно задать максимальный размер ключа. Усечение ключа важно, так как это может повлиять на то, что строки считаются разными. если этот параметр имеет значение 0 или 255, то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003. Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра [датабасепажесизе](./jet-param-enumeration.md). Дополнительные сведения см. в разделе [кэймост](./vistaparam.keymost-field.md) .

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Элементы JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
