---
title: Клоседкаптион. Жетсамистиленаме, метод
description: Метод Жетсамистиленаме извлекает имя стиля, поддерживаемого текущим файлом SAMI.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- Жетсамистиленаме метод Windows Media Player
- Жетсамистиленаме метод Windows Media Player, класс Клоседкаптион
- Класс Клоседкаптион Windows Media Player, метод Жетсамистиленаме
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694876"
---
# <a name="closedcaptiongetsamistylename-method"></a>Клоседкаптион. Жетсамистиленаме, метод

Метод **жетсамистиленаме** извлекает имя стиля, поддерживаемого текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**длинное**), определяющее индекс извлекаемого имени стиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку** , содержащую имя стиля, как указано в файле Sami.

## <a name="remarks"></a>Комментарии

Стили в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.

Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

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

[**Клоседкаптион. Самистиле**](closedcaption-samistyle.md)
</dt> </dl>

 

 





