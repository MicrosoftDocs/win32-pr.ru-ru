---
description: 'Дополнительные сведения о методе: Дураблекоммиткаллбакк. Релеасересаурце'
title: Дураблекоммиткаллбакк. Релеасересаурце, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272721"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>Дураблекоммиткаллбакк. Релеасересаурце, метод

Освобождает сеанс долговременной фиксации.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a>Примечания

Не пытайтесь присвоить параметру экземпляра значение null, так как обратный вызов удаляется после Жеттерм, а обратный вызов не может быть установлен после Жеттерм.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Дураблекоммиткаллбакк](./durablecommitcallback-class.md)

[Элементы Дураблекоммиткаллбакк](./durablecommitcallback-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
