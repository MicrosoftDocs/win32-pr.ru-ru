---
title: Ивмпсеттингс. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) возвращает значение, указывающее, можно ли выполнить указанное действие.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- Проигрыватель Windows Media Ивмпсеттингс. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694658"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>Ивмпсеттингс. доступ (VB и C#)

Свойство **Available** (метод Get- **\_ Available** в C#) возвращает значение, указывающее, можно ли выполнить указанное действие.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Параметры

*бстритем*

**Строка System. String** , которая является одним из следующих значений.



| Значение              | Описание                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| автозапуск          | Обнаруживает, можно ли задать свойство автозапуска, чтобы указать, что проигрыватель Windows Media автоматически запускает воспроизведение. |
| Balance            | Обнаруживает, можно ли использовать свойство Balance для установки баланса стерео.                                           |
| BaseURL            | Обнаруживает, можно ли задать свойство baseURL для указания базового URL-адреса.                                                |
| дефаултфраме       | Обнаруживает, можно ли задать свойство Дефаултфраме, чтобы указать кадр по умолчанию.                                    |
| енаблиррордиалогс | Обнаруживает, можно ли установить свойство Енаблиррордиалогс для включения или отключения отображения диалоговых окон ошибок.        |
| Режим            | Обнаруживает, можно ли использовать метод метода мода для получения текущего цикла или режима "в случайном порядке".                          |
| инвокеурлс         | Обнаруживает, можно ли задать свойство Инвокеурлс, чтобы указать, должны ли события URL запускаться в веб-браузере.         |
| Mute               | Обнаруживает, можно ли задать свойство «выкл.», чтобы указать, включены ли звуковые выходные данные.                        |
| плайкаунт          | Обнаруживает, можно ли задать свойство Плайкаунт, чтобы указать число попыток воспроизведения элемента мультимедиа.                 |
| Тариф               | Обнаруживает, можно ли задать свойство Rate для управления скоростью воспроизведения.                                            |
| SetMode            | Обнаруживает, можно ли использовать метод setMode для указания текущего цикла или режима "в случайном порядке".                           |
| Том             | Обнаруживает, можно ли задать для свойства Volume громкость звука.                                           |



 

## <a name="property-value"></a>Значение свойства

Значение **System. Boolean** , указывающее, можно ли выполнить указанное действие.

## <a name="remarks"></a>Комментарии

**Ивмпсеттингс. идентично** — это свойство в Visual Basic, которое принимает параметр. В C# он называется **ивмпсеттингс. Get \_ тождественным** методом.

## <a name="examples"></a>Примеры

В следующем примере каждый из свойств **ивмпсеттингс** проверяется с помощью свойства **Available** (метод **Get- \_ Available** в C#). Имя свойства и результат каждого теста отображаются в многострочном текстовом поле. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





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

[**Ивмпсеттингс. Автозапуск (VB и C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Balance (VB и C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. baseURL (VB и C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Дефаултфраме (VB и C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. мода (VB и C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Инвокеурлс (VB и C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. выкл. (VB и C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Плайкаунт (VB и C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. rate (VB и C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. setMode (VB и C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Volume (VB и C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





