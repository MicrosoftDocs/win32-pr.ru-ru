---
title: IWMPClosedCaption2 Самилангкаунт, свойство
description: Свойство Самилангкаунт возвращает количество языков, поддерживаемых текущим файлом SAMI.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- проигрыватель Windows Media свойства самилангкаунт
- проигрыватель Windows Media свойства самилангкаунт, интерфейс IWMPClosedCaption2
- проигрыватель Windows Media интерфейса IWMPClosedCaption2, свойство самилангкаунт
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
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900004"
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

## <a name="remarks"></a>Remarks

Это свойство возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).

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

[**Ивмпклоседкаптион. Самиланг (VB и C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. Жетсамилангнаме (VB и C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





