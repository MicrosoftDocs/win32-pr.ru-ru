---
description: Дополнительные сведения о перечислении Стопсервицегрбит
title: Перечисление Стопсервицегрбит (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477460"
---
# <a name="stopservicegrbit-enumeration"></a>Перечисление Стопсервицегрбит

Параметры для [JetStopServiceInstance2 (JET_INSTANCE, стопсервицегрбит)](./windows8api.jetstopserviceinstance2-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Члены


|  | Имя участника | Описание | 
|--|-------------|-------------|
|  | Все | Останавливает все службы ESE для указанного экземпляра. | 
|  | баккграундусертаскс | Останавливает Перезапускаемые клиентские задачи фонового обслуживания (дефрагментацию B + Tree). | 
|  | куиесцекачес | Куиесцес все "грязные" кэши на диск. Асинхронная. Замораживание отменяется, если впоследствии вызывается бит возобновления. | 
|  | Возобновить | Возобновляет ранее выданные операции выхода, т. е. "перезапускает службу". Можно сочетать с грбитс, чтобы возобновить работу конкретных служб, или с параметром 0x0 возобновляет работу всех предыдущих остановленных служб.<p>Предупреждение. Этот бит можно использовать только для возобновления JET_bitStopServiceBackground и JET_bitStopServiceQuiesceCaches, если вы выполняли JET_bitStopServiceAll или JET_bitStopServiceAPI, попытка использовать JET_bitStopServiceResume завершится ошибкой.</p> | 



## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
