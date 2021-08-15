---
title: Ивмпмедиа getItemInfo, метод
description: Метод getItemInfo возвращает значение указанного атрибута для элемента мультимедиа.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- проигрыватель Windows Media метода getItemInfo
- проигрыватель Windows Media метода getItemInfo, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8fa8b55074781dd835e116b0403391fe9343af30d5236610219dca8aba810b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331994"
---
# <a name="iwmpmediagetiteminfo-method"></a>Метод Ивмпмедиа:: getItemInfo

Метод **getItemInfo** возвращает значение указанного атрибута для элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритемнаме* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является значением указанного атрибута.

## <a name="remarks"></a>Remarks

Этот метод возвращает метаданные для отдельного элемента мультимедиа или элемента мультимедиа, который является частью списка воспроизведения.

Свойство **аттрибутекаунт** возвращает количество имен атрибутов, доступных для данного элемента мультимедиа. Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имени каждого доступного атрибута. Имена отдельных атрибутов можно передать в **getItemInfo**.

Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .

Если элемент мультимедиа получен из библиотеки, полученной путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), набор доступных атрибутов будет отличаться от тех, которые можно запрашивать из локальной библиотеки, полученной путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Например, атрибуты, доступные из локальной библиотеки, извлеченной с помощью **ивмплибрари** , будут подмножеством атрибутов, доступных из локальной библиотеки, полученной с помощью **ивмпкоре**. Набор атрибутов, доступных из других источников (удаленных библиотек, переносных устройств или компакт-дисков), определяется другими источниками.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Аттрибутекаунт (VB и C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Жетаттрибутенаме (VB и C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Сетитеминфо (VB и C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. Жетитеминфобитипе (VB и C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





