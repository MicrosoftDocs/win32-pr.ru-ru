---
title: Ивмпсеттингс setMode, метод
description: Метод setMode устанавливает активный или неактивный режим цикла или случайного режима.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- проигрыватель Windows Media метода setMode
- проигрыватель Windows Media метода setMode, интерфейс ивмпсеттингс
- проигрыватель Windows Media интерфейса ивмпсеттингс, метод setMode
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
ms.openlocfilehash: 529aadf412cdae869ae3c308d82dcd08a7dfd581aeb7ecc711052f6acd54b962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568411"
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

## <a name="remarks"></a>Remarks

когда активен режим шовфраме, проигрыватель Windows Media должен получить доступ к содержимому дорожки для получения видеокадра. Используйте этот режим с осторожностью при воспроизведении содержимого, которое не является локальным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. мода (VB и C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





