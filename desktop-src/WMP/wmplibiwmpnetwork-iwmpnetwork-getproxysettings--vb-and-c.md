---
title: Ивмпнетворк Жетпроксисеттингс, метод
description: Метод Жетпроксисеттингс возвращает сведения о параметрах прокси-сервера для протокола.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Жетпроксисеттингс метод Windows Media Player
- Жетпроксисеттингс метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксисеттингс
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668850"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>Метод Ивмпнетворк:: Жетпроксисеттингс

Метод **жетпроксисеттингс** возвращает сведения о параметрах прокси-сервера для протокола.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрпротокол* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Int32** , которое является одним из следующих значений.



| Значение | Описание                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Прокси-сервер не используется.                                                |
| 1     | Используются параметры прокси-сервера для текущего браузера (допустимы только для HTTP). |
| 2     | Используются заданные вручную параметры прокси-сервера.                            |
| 3     | Параметры прокси-сервера обнаруживаются в автоматическом режиме.                                      |



 

## <a name="remarks"></a>Комментарии

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

## <a name="examples"></a>Примеры

В следующем примере кода используется **жетпроксисеттингс** для вывода сообщения, которое предоставляет сведения о текущих параметрах прокси-сервера проигрывателя в метке. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Ивмпнетворк. setProxySettings (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





