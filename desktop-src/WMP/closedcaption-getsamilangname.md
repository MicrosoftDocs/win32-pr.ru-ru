---
title: Клоседкаптион. Жетсамилангнаме, метод
description: Метод Жетсамилангнаме извлекает имя языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- проигрыватель Windows Media метода жетсамилангнаме
- проигрыватель Windows Media метода жетсамилангнаме, класс клоседкаптион
- класс клоседкаптион проигрыватель Windows Media, метод жетсамилангнаме
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764034"
---
# <a name="closedcaptiongetsamilangname-method"></a>Клоседкаптион. Жетсамилангнаме, метод

Метод **жетсамилангнаме** извлекает имя языка, поддерживаемого текущим файлом Sami.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**длинное**), определяющее индекс имени языка для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку** , содержащую имя языка, указанное в файле Sami.

## <a name="remarks"></a>Remarks

Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.

Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> <dt>

[**Клоседкаптион. Самиланг**](closedcaption-samilang.md)
</dt> </dl>

 

 





