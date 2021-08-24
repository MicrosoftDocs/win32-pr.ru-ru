---
title: IWMPClosedCaption2 Жетсамистиленаме, метод
description: Метод Жетсамистиленаме возвращает имя стиля, поддерживаемого текущим файлом SAMI.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- проигрыватель Windows Media метода жетсамистиленаме
- проигрыватель Windows Media метода жетсамистиленаме, интерфейс IWMPClosedCaption2
- проигрыватель Windows Media интерфейса IWMPClosedCaption2, метод жетсамистиленаме
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd599370afb9029a481fbae33264796232e4f129c1a5da0d2658452b785a870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031354"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>Метод IWMPClosedCaption2:: Жетсамистиленаме

Метод **жетсамистиленаме** возвращает имя стиля, поддерживаемого текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ниндекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является начинающимся с нуля индексом имени стиля для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является именем стиля, как указано в файле Sami.

## <a name="remarks"></a>Remarks

Стили в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.

Этот метод возвращает строку нулевой длины (""), если файл мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Ивмпклоседкаптион. Самистиле (VB и C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





