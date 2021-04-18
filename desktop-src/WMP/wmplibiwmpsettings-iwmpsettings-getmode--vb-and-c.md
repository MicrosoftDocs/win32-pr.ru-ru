---
title: Ивмпсеттингс, метод
description: Метод метода мода возвращает значение, указывающее, активен ли режим "цикл" или "случайный".
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- метод мода проигрыватель Windows Media
- метод onmode проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, методического режима
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717907"
---
# <a name="iwmpsettingsgetmode-method"></a>Метод Ивмпсеттингс:: onmode

Метод метода **мода** возвращает значение, указывающее, активен ли режим "цикл" или "случайный".

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрмоде* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является одним из следующих значений.



| Значение      | Описание                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| ауторевинд | Дорожки перезапускаются с начала после воспроизведения до конца.                                |
| loop       | Последовательность дорожек повторяется самим собой.                                                           |
| шовфраме  | Ближайший ключевой кадр отображается, когда не воспроизводится. Этот режим не подходит для звуковых дорожек. |
| shuffle    | Дорожки воспроизводятся в случайном порядке.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , указывающее, активен ли заданный режим.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. setMode (VB и C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





