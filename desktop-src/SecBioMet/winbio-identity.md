---
title: Структура WINBIO_IDENTITY (Винбио \_ types. h)
description: Содержит идентифицирующее значение, связанное с биометрической шаблоном.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API структуры WINBIO_IDENTITY биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677a341386bcc937061798f406397028c23c10b65989480da975a9fdf81a3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910122"
---
# <a name="winbio_identity-structure"></a>\_Структура идентификации винбио

Структура **\_ удостоверения винбио** содержит идентифицирующее значение, связанное с биометрической шаблоном.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Члены

<dl> <dt>

**Type**
</dt> <dd>

Задает формат сведений об удостоверении, содержащихся в этой структуре. Может иметь одно из следующих значений:



| Значение                                                                                                                                                                                         | Значение                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_тип идентификатора \_ винбио \_ null**</dt> </dl>             | Шаблон не имеет связанного идентификатора.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ шаблон типа идентификатора \_ винбио**</dt> </dl> | Структура соответствует всем удостоверениям шаблона.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_ \_ GUID типа идентификатора \_ винбио**</dt> </dl>             | Структура содержит идентификатор GUID, связанный с шаблоном.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**ИД \_ \_ безопасности типа \_ идентификатора винбио**</dt> </dl>                | Структура содержит идентификатор безопасности учетной записи, связанный с шаблоном.<br/> |



 

</dd> <dt>

**Значение**
</dt> <dd>

Объединение, которое может содержать одно из следующих значений:

<dl> <dt>

**Null**
</dt> <dd>

Содержит 1, если член **типа** имеет **\_ тип винбио \_ ID \_ null**.

</dd> <dt>

**Подстановочный знак**
</dt> <dd>

Содержит значение 1, если член **типа** имеет **\_ \_ \_ подстановочный знак винбио типа ID**.

</dd> <dt>

**темплатегуид**
</dt> <dd>

Содержит 128-разрядное значение идентификатора GUID, идентифицирующее шаблон, если член **типа** имеет тип **винбио \_ ID \_ \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Структура, содержащая идентификатор безопасности учетной записи, если член **типа** имеет **\_ тип винбио ID \_ \_ SID**.

<dl> <dt>

**Размер**
</dt> <dd>

Число символов в SID.

</dd> <dt>

**Данные**
</dt> <dd>

Массив неподписанных символов, содержащих идентификатор безопасности. Текущий максимальный размер массива составляет 68 символов.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется в следующих функциях:

-   [**винбиоделететемплате**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**винбиоенроллкоммит**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**винбиоенуменроллментс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**винбиоидентифи**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**винбиоремовекредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**винбиоверифи**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**винбиоверифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры клиентских приложений](client-application-structures.md)
</dt> </dl>

 

 





