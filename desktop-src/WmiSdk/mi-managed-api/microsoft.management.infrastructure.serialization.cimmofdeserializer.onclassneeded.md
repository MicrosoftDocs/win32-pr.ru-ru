---
description: 'Дополнительные сведения о: Циммофдесериализер. Онкласснидед Delegate (строка, строка, строка)'
title: Делегат CimMofDeserializer.OnClassNeeded (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 50e107c09eccde03446278516a1f125f4ad86022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719412"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a>Циммофдесериализер. Онкласснидед-делегат (строка, строка, строка)

Представляет обратный вызов для получения класса CIM для указанного сервера, пространства имен и имени класса.

**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Синтаксис

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a>Параметры

  - serverName  
    Тип: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Имя сервера для класса CIM.

<!-- end list -->

  - namespaceName  
    Тип: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Имя пространства имен для класса CIM.

<!-- end list -->

  - className  
    Тип: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Имя класса для класса CIM.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [класс Цимкласс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))

Возвращает класс CIM, соответствующий указанным аргументам, или **значение NULL** , если класс не найден.

## <a name="see-also"></a>См. также:

[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
