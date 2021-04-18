---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. Кбварсегмак'
title: Свойство JET_OPENTEMPORARYTABLE. Кбварсегмак (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702352"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a>Свойство JET_OPENTEMPORARYTABLE. Кбварсегмак

Возвращает или задает максимальный объем данных, который будет использоваться из любой переменной ленгсколумн для создания ключа для данной строки. Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом. Это ограничение указано в байтах. Если этот параметр равен нулю или имеет то же значение, что и свойство [кбкэймост](./jet-opentemporarytable.cbkeymost-property.md) , ограничение не действует.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Элементы JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
