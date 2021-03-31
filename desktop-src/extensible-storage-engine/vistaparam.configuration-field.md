---
description: 'Дополнительные сведения о: VistaParam.Configполе фигурации'
title: VistaParam.Configполе фигурации (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808422"
---
# <a name="vistaparamconfiguration-field"></a>VistaParam.Configполе фигурации

Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров. Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации. Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию. Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти. Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Вистапарам](./vistaparam-class.md)

[Элементы Вистапарам](./vistaparam-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
