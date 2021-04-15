---
title: IWMPClosedCaption2 Жетсамилангнаме, метод
description: Метод Жетсамилангнаме возвращает имя языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Жетсамилангнаме метод Windows Media Player
- Жетсамилангнаме метод проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, метод Жетсамилангнаме
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689318"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>Метод IWMPClosedCaption2:: Жетсамилангнаме

Метод **жетсамилангнаме** возвращает имя языка, поддерживаемого текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ниндекс* \[ окне\]
</dt> <dd>

**Объект System. Int32** , который является начинающимся с нуля индексом имени языка для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая представляет собой имя языка, указанное в файле Sami.

## <a name="remarks"></a>Комментарии

Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.

Этот метод возвращает строку нулевой длины (""), если файл мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Ивмпклоседкаптион. Самиланг (VB и C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





