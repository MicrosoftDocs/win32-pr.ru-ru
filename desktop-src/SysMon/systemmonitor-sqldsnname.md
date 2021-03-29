---
title: Системмонитор Склдсннаме, свойство
description: Возвращает или задает имя источника данных ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Сисмон свойство Склдсннаме
- Свойство Склдсннаме Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, свойство Склдсннаме
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414701"
---
# <a name="systemmonitorsqldsnname-property"></a>Свойство Системмонитор:: Склдсннаме

Возвращает или задает имя источника данных ODBC (DSN).

## <a name="syntax"></a>Синтаксис


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Значение свойства

Имя источника данных ODBC, указывающее на базу данных, содержащую правильные таблицы Perfmon. Формат — SQL: DSN.

## <a name="remarks"></a>Комментарии

Для создания файла журнала SQL необходимо использовать оснастку MMC Perfmon. msc. Журналы счетчиков находятся в разделе **журналы и оповещения производительности**. Чтобы указать журнал SQL, щелкните правой кнопкой мыши созданный файл журнала и выберите в меню пункт **Свойства** . На странице свойств **файлы журнала** выберите **база данных SQL** в раскрывающемся списке **Тип файла журнала** .

**До Windows Vista:** Нельзя изменить это свойство, если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение [**DataSourceTypeConstants.sysмонскллог**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Сначала необходимо указать имя, а затем задать **системмонитор. DataSourceType** в **DataSourceTypeConstants.sysмонскллог**.

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

[**Системмонитор. Скллогсетнаме**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





