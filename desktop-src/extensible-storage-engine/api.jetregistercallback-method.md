---
description: Дополнительные сведения о методе API. Жетрегистеркаллбакк
title: API. Жетрегистеркаллбакк, метод
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703157"
---
# <a name="apijetregistercallback-method"></a>API. Жетрегистеркаллбакк, метод

Позволяет приложению настроить ядро СУБД на выдачу уведомлений для конкретных событий в приложении. Эти уведомления связаны с определенной таблицей и остаются в силе только до тех пор, пока экземпляр, содержащий таблицу, не завершит работу с помощью [жеттерм (JET_INSTANCE)](./api.jetterm-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, Открытый в таблице, в которой должен быть зарегистрирован обратный вызов.

<!-- end list -->

  - кбтип  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    Причины обратного вызова, для которых приложение хочет получать уведомления.

<!-- end list -->

  - обратный вызов  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Функция обратного вызова.

<!-- end list -->

  - контекст  
    Тип: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Контекст, который будет передан обратному вызову.

<!-- end list -->

  - каллбаккид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Маркер, который впоследствии можно использовать для отмены регистрации заданной функции обратного вызова с помощью [жетунрегистеркаллбакк (JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
