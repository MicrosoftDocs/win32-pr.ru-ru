---
title: Системмонитор. Лоадсеттингс, метод
description: Добавляет счетчики из HTML-файла шаблона в системный монитор.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Метод Лоадсеттингс Сисмон
- Метод Лоадсеттингс Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Лоадсеттингс
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415584"
---
# <a name="systemmonitorloadsettings-method"></a>Системмонитор. Лоадсеттингс, метод

Добавляет счетчики из HTML-файла шаблона в системный монитор.

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сеттингсфиленаме* \[ окне\]
</dt> <dd>

Строка HTML, указывающая счетчики, которые необходимо добавить в системный монитор.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Чтобы сохранить текущие счетчики в системном мониторе в HTML-файл, вызовите метод [**системмонитор. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> </dl>

 

 





