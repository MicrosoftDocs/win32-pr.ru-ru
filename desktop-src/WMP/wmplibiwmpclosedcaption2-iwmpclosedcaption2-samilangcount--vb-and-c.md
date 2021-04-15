---
title: IWMPClosedCaption2 Самилангкаунт, свойство
description: Свойство Самилангкаунт возвращает количество языков, поддерживаемых текущим файлом SAMI.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Проигрыватель Windows Media для свойства Самилангкаунт
- Самилангкаунт свойство проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, свойство Самилангкаунт
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689316"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>Свойство IWMPClosedCaption2:: Самилангкаунт

Свойство **самилангкаунт** возвращает количество языков, поддерживаемых текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является числом поддерживаемых языков.

## <a name="remarks"></a>Комментарии

Это свойство возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).

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
</dt> <dt>

[**IWMPClosedCaption2. Жетсамилангнаме (VB и C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





