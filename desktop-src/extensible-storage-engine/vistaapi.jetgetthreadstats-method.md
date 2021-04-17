---
description: 'Дополнительные сведения о методе: Вистаапи. Жетжетсреадстатс'
title: Вистаапи. Жетжетсреадстатс, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701903"
---
# <a name="vistaapijetgetthreadstats-method"></a>Вистаапи. Жетжетсреадстатс, метод

Получает сведения о производительности из ядра СУБД для текущего потока. Для сбора статистики, отражающей активность ядра СУБД в этом потоке между этими вызовами, можно использовать несколько вызовов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a>Параметры

  - среадстатс  
    Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Возвращает статистические данные потока.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Вистаапи](./vistaapi-class.md)

[Элементы Вистаапи](./vistaapi-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
