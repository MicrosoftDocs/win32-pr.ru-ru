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
ms.openlocfilehash: 387bf2e42475d27f5440afb3fa0b945c910b3ac3bad610495936cd3a4a900bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882329"
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

## <a name="remarks"></a>Remarks

Чтобы сохранить текущие счетчики в системном мониторе в HTML-файл, вызовите метод [**системмонитор. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> </dl>

 

 





