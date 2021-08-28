---
title: Ивмпсеттингс, метод
description: Метод метода мода возвращает значение, указывающее, активен ли режим "цикл" или "случайный".
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- метод в режиме проигрыватель Windows Media
- метод проигрыватель Windows Media, интерфейс ивмпсеттингс
- интерфейс ивмпсеттингс проигрыватель Windows Media, методического режима
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
ms.openlocfilehash: fae5d910dbbdf1fc2241a63dcf6c61c94e968cf0f2b36316407aafc8fc5f2dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246304"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. setMode (VB и C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





