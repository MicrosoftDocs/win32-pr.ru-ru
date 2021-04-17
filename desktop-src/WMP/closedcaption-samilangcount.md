---
title: Клоседкаптион. Самилангкаунт
description: Свойство Самилангкаунт извлекает количество языков, поддерживаемых текущим файлом SAMI.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самилангкаунт
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694872"
---
# <a name="closedcaptionsamilangcount"></a>Клоседкаптион. Самилангкаунт

Свойство **самилангкаунт** извлекает количество языков, поддерживаемых текущим файлом Sami.

``` syntax
player.closedCaption.SAMILangCount
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

[**Клоседкаптион. Жетсамилангнаме**](closedcaption-getsamilangname.md)
</dt> <dt>

[**Клоседкаптион. Самиланг**](closedcaption-samilang.md)
</dt> </dl>

 

 





