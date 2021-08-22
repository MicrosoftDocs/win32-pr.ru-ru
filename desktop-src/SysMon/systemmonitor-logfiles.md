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
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882184"
---
# <a name="systemmonitorlogfiles-property"></a>Системмонитор. файл_журнала, свойство

Коллекция из одного или нескольких файлов журнала, используемых в качестве источника значений счетчиков, отображаемых в системном мониторе.

## <a name="syntax"></a>Синтаксис


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Значение свойства

Коллекция объектов [**логфилеитем**](logfileitem.md) , которые указывают файлы журналов, используемые в качестве источника данных для графа.

## <a name="remarks"></a>Remarks

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

 

 





