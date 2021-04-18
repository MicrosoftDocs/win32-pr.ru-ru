---
title: Клоседкаптион. Самистилекаунт
description: Свойство Самистилекаунт извлекает количество стилей, поддерживаемое текущим файлом SAMI.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самистилекаунт
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
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694560"
---
# <a name="closedcaptionsamistylecount"></a>Клоседкаптион. Самистилекаунт

Свойство **самистилекаунт** извлекает количество стилей, поддерживаемое текущим файлом Sami.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).

**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
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

 

 





