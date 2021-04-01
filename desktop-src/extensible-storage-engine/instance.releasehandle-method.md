---
description: Дополнительные сведения о методе instance. ReleaseHandle
title: Экземпляр. ReleaseHandle, метод
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fcac0fcbffc685fb91bd0c0bf2f97865540cb1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081204"
---
# <a name="instancereleasehandle-method"></a>Экземпляр. ReleaseHandle, метод

Освобождение маркера для этого экземпляра.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если можно освободить маркер.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Члены экземпляра](./instance-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
