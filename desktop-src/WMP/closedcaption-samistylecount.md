---
title: Клоседкаптион. Самистилекаунт
description: Свойство Самистилекаунт извлекает количество стилей, поддерживаемое текущим файлом SAMI.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- клоседкаптион. самистилекаунт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e5563e40fabfa2cc82dc24598414f312192f864ecacd6ed743834e12e06759
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119525"
---
# <a name="closedcaptionsamistylecount"></a>Клоседкаптион. Самистилекаунт

Свойство **самистилекаунт** извлекает количество стилей, поддерживаемое текущим файлом Sami.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).

**проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> <dt>

[**Клоседкаптион. Жетсамистиленаме**](closedcaption-getsamistylename.md)
</dt> <dt>

[**Клоседкаптион. Самистиле**](closedcaption-samistyle.md)
</dt> </dl>

 

 





