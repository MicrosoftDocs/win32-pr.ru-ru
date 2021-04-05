---
title: Метод LogFile. Remove
description: Удаляет указанный экземпляр Логфилеитем из коллекции.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Удалить метод Сисмон
- Remove Method Сисмон, класс файл_журнала
- Файл_журнала класса Сисмон, Remove, метод
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803352"
---
# <a name="logfilesremove-method"></a>Метод LogFile. Remove

Удаляет указанный экземпляр [**логфилеитем**](logfileitem.md) из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Целочисленный индекс файла журнала, который необходимо удалить из коллекции. Индекс основан на единицах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

**До Windows Vista:** Невозможно удалить файлы журнала из [**коллекции файлов журнала**](systemmonitor-logfiles.md) , если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение сисмонлогфилес.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**логфилеитем**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





