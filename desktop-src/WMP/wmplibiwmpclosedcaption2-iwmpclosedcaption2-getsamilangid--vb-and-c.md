---
title: IWMPClosedCaption2 Жетсамилангид, метод
description: Метод Жетсамилангид возвращает код локали (LCID) языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- проигрыватель Windows Media метода жетсамилангид
- проигрыватель Windows Media метода жетсамилангид, интерфейс IWMPClosedCaption2
- проигрыватель Windows Media интерфейса IWMPClosedCaption2, метод жетсамилангид
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0fc62222f98d6c056bb8ce9ffd328582a6764202bb8446617471d3f7cb4a5ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506434"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>Метод IWMPClosedCaption2:: Жетсамилангид

Метод **жетсамилангид** возвращает код локали (LCID) языка, поддерживаемого текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ниндекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является начинающимся с нуля индексом LCID для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект **System. Int32** , который является LCID языка с указанным индексом.

## <a name="remarks"></a>Remarks

Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.

Этот метод возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).

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

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





