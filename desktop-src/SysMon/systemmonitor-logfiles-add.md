---
title: Файл журнала. Add, метод
description: Добавляет файл журнала в коллекцию.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Добавить метод Сисмон
- Метод Add Сисмон, класс LogFile
- Файл_журнала класса Сисмон, Add метод
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af01c5c7a1bbe16826457d7e1f8700df01876827c522a36db41f6c3843101d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882339"
---
# <a name="logfilesadd-method"></a>Файл журнала. Add, метод

Добавляет файл журнала в коллекцию.

## <a name="syntax"></a>Синтаксис


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*путь к файлу* \[ окне\]
</dt> <dd>

Путь к файлу журнала. Путь можно указать как абсолютный, относительный или UNC-путь. Имя файла журнала должно быть либо .csv, TSV, либо. blg.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для создания файлов журналов, добавляемых в эту коллекцию, необходимо использовать средство Logman.exe или оснастку MMC Perfmon. msc. Для Perfmon. msc журналы счетчиков находятся в папке **журналы и оповещения производительности**. Дополнительные сведения об использовании Logman.exe или Perfmon. msc см. в подокне **центра справки и поддержки**, которое можно найти по программе Logman.

**до Windows Vista:** Невозможно добавить файлы журнала в [**коллекцию файлов журнала**](systemmonitor-logfiles.md) , если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение [**DataSourceTypeConstants.sysмонлогфилес**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Сначала задайте **системмонитор. DataSourceType** для **DataSourceTypeConstants.sysмоннуллдатасаурце**, добавьте файлы журнала и счетчики, а затем установите **Системмонитор. DataSourceType** в **DataSourceTypeConstants.sysмонлогфилес**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**логфилеитем**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





