---
description: Дополнительные сведения о методе API. Жетжетаттачинфоинстанце
title: API. Жетжетаттачинфоинстанце, метод
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719323"
---
# <a name="apijetgetattachinfoinstance-method"></a>API. Жетжетаттачинфоинстанце, метод

Используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)](./api.jetbeginexternalbackupinstance-method.md) , для запроса экземпляров имен файлов базы данных, которые должны быть частью набора файлов резервной копии. Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью [жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)](./api.jetattachdatabase-method.md) . Эти файлы впоследствии можно открыть с помощью [жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) и считывать с помощью [жетреадфилеинстанце (JET_INSTANCE, JET_HANDLE, \[ \] Int32, Int32)](./api.jetreadfileinstance-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Параметры

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр, для которого необходимо получить сведения.

<!-- end list -->

  - files  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Возвращает список строк, заканчивающихся нулем, описывающих набор файлов базы данных, который должен быть частью набора файлов резервной копии. Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром. Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.

<!-- end list -->

  - maxChars  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Максимальное число извлекаемых символов.

<!-- end list -->

  - актуалчарс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Фактический размер списка файлов. Если это значение больше maxChars, список был обрезан.

## <a name="remarks"></a>Комментарии

Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
