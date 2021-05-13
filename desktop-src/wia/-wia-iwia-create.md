---
description: Метод Create объекта WIA устанавливает соединение с указанным устройством для получения образа Windows (WIA) и возвращает объект Item, представляющий устройство.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Метод WIA. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841335"
---
# <a name="wiacreate-method"></a>Метод WIA. Create

Метод **CREATE** объекта [**WIA**](-wia-wia.md) устанавливает соединение с указанным устройством для получения образа Windows (WIA) и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Устройство* \[ окне\]
</dt> <dd>

Тип: **Variant \***

Указывает устройство WIA, к которому необходимо подключиться.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **ивиадиспатчитем**

В случае успешного выполнения этот метод возвращает объект [**Item**](-wia-item.md) , представляющий аппаратное устройство WIA (корневой элемент).

## <a name="remarks"></a>Remarks

Параметр *Device* указывает объект [**DeviceInfo**](-wia-deviceinfo.md) , передавая сам объект, его индекс из объекта Collection или значение свойства [**ID**](-wia-iwiadeviceinfo-id.md) . **Ничего не** передавать, чтобы отобразить диалоговое окно, позволяющее пользователю выбрать устройство.

## <a name="examples"></a>Примеры

В следующих примерах на языке VBScript показано использование метода **CREATE** .

В первом примере объект [**DeviceInfo**](-wia-deviceinfo.md) передается в метод **CREATE** . Обратите внимание, что передача свойства [**ID**](-wia-iwiadeviceinfo-id.md) объекта вызывает точно такое же поведение.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



В следующем примере вызывающее приложение передает индекс объекта [**DeviceInfo**](-wia-deviceinfo.md) в коллекции в метод **CREATE** .


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



В следующем примере **ничего не** передается в метод **CREATE** , чтобы отобразить диалоговое окно, позволяющее пользователю выбрать устройство.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




