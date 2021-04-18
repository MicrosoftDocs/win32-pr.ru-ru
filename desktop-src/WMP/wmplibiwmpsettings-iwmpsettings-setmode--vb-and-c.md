---
title: Ивмпсеттингс setMode, метод
description: Метод setMode устанавливает активный или неактивный режим цикла или случайного режима.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setMode метод Windows Media Player
- setMode метод проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, метод setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717783"
---
# <a name="iwmpsettingssetmode-method"></a>Метод Ивмпсеттингс:: setMode

Метод **setMode** устанавливает активный или неактивный режим цикла или случайного режима.

## <a name="syntax"></a>Синтаксис


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрмоде* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем изменяемого режима, содержащего одно из следующих значений.



| Значение      | Описание                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| ауторевинд | Дорожки перезапускаются с начала после воспроизведения до конца.                                |
| loop       | Последовательность дорожек повторяется самим собой.                                                           |
| шовфраме  | Ближайший ключевой кадр отображается, когда не воспроизводится. Этот режим не подходит для звуковых дорожек. |
| shuffle    | Дорожки воспроизводятся в случайном порядке.                                                               |



 

</dd> <dt>

*варфмоде* \[ окне\]
</dt> <dd>

Значение **System. Boolean** , указывающее, активен ли новый заданный режим.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Когда активен режим Шовфраме, проигрыватель Windows Media должен получить доступ к содержимому дорожки, чтобы получить кадр видео. Используйте этот режим с осторожностью при воспроизведении содержимого, которое не является локальным.

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

[**Ивмпсеттингс. мода (VB и C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





