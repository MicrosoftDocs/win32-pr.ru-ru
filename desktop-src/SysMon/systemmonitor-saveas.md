---
title: Системмонитор. SaveAs, метод
description: Сохраняет значения счетчиков в представлении графа в файле журнала.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs, метод Сисмон
- Метод SaveAs Сисмон, объект Системмонитор
- Системмонитор объекта Сисмон, метод SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661887"
---
# <a name="systemmonitorsaveas-method"></a>Системмонитор. SaveAs, метод

Сохраняет значения счетчиков в представлении графа в файле журнала.

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя файла* \[ окне\]
</dt> <dd>

Путь к файлу журнала. Путь можно указать как абсолютный, относительный или UNC-путь. Имя файла журнала должно быть либо. TSV, либо htm. Если папка в пути не существует, СИСМОН создаст ее. Если файл существует, файл перезаписывается. СИСМОН применяет ACL по умолчанию из родительского каталога.

</dd> <dt>

*тип* \[ файла окне\]
</dt> <dd>

Формат данных счетчиков, сохраненных в файле журнала. Можно указать либо [**SysmonFileType.sysмонфилехтмл**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) , либо **SysmonFileType.sysмонфилетсв**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Сохраняются только данные счетчиков, видимые в представлении графа (фактическое число сохраняемых точек данных, см. в разделе [**системмонитор. датапоинткаунт**](systemmonitor-datapointcount.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> <dt>

[**Системмонитор. Relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





