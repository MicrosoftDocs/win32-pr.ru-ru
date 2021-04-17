---
title: Системмонитор. файл_журнала, свойство
description: Коллекция из одного или нескольких файлов журнала, используемых в качестве источника значений счетчиков, отображаемых в системном мониторе.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Свойства файлов журнала Сисмон
- Свойство Файл_журналаs Сисмон, объект Системмонитор
- Системмонитор объекта Сисмон, свойство файл_журнала
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661891"
---
# <a name="systemmonitorlogfiles-property"></a>Системмонитор. файл_журнала, свойство

Коллекция из одного или нескольких файлов журнала, используемых в качестве источника значений счетчиков, отображаемых в системном мониторе.

## <a name="syntax"></a>Синтаксис


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Значение свойства

Коллекция объектов [**логфилеитем**](logfileitem.md) , которые указывают файлы журналов, используемые в качестве источника данных для графа.

## <a name="remarks"></a>Комментарии

Чтобы добавить или удалить файл журнала из коллекции файлов журнала, значение [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) не должно быть установлено в сисмонлогфилес.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> <dt>

[**Системмонитор. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**Системмонитор. Логвиевстарт**](systemmonitor-logviewstart.md)
</dt> <dt>

[**Системмонитор. Логвиевстоп**](systemmonitor-logviewstop.md)
</dt> <dt>

[**Системмонитор. Скллогсетнаме**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





