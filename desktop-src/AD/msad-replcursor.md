---
title: Класс MSAD_ReplCursor
description: Предоставляет сведения о состоянии входящей репликации о всех репликах заданного контекста именования (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplCursor Active Directory
- Active Directory класса MSAD_ReplCursor, описание
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490737"
---
# <a name="msad_replcursor-class"></a>\_Класс МСАД реплкурсор

Предоставляет сведения о состоянии входящей репликации о всех репликах заданного контекста именования (NC).

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>Члены

Класс **МСАД \_ реплкурсор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **МСАД \_ реплкурсор** имеет следующие свойства.

<dl> <dt>

**намингконтекстдн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает путь X. 500 для контекста именования (NC), содержащего этот курсор.

</dd> <dt>

**саурцедсадн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает путь X. 500 к системному агенту каталога (DSA), который представляет исходный контроллер домена (DC).

</dd> <dt>

**саурцедсаинвокатионид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает идентификатор вызова исходного сервера, которому соответствует **уснаттрибутефилтер** .

</dd> <dt>

**тимеофластсукцессфулсинк**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает метку времени последней успешной синхронизации репликации с исходным DSA. Указывает время, в течение которого этот контроллер домена покажет изменения, внесенные в исходный DSA для этого сетевого контроллера.

</dd> <dt>

**уснаттрибутефилтер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает максимальный порядковый номер обновления, по которому целевой сервер может указать, что он записал все изменения, порожденные данным сервером, по порядковым номерам обновления, меньшим или равным, этим порядковым номером обновления. Это свойство используется для фильтрации изменений, которые сервер назначения уже применил к исходным серверам репликации.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_курсор REPL в DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

