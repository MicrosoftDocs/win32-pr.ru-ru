---
title: Controls. Жетаудиолангуажедескриптион, метод
description: Метод Жетаудиолангуажедескриптион Извлекает описание для языкового аудио, соответствующего указанному индексу, основанному на единице.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Жетаудиолангуажедескриптион метод Windows Media Player
- метод Жетаудиолангуажедескриптион Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Жетаудиолангуажедескриптион
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694849"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls. Жетаудиолангуажедескриптион, метод

Метод **жетаудиолангуажедескриптион** Извлекает описание для языкового аудио, соответствующего указанному индексу, основанному на единице.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**длинное целое**), указывающее индекс языкового аудио на основе единицы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строковое** значение.

## <a name="remarks"></a>Комментарии

Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.

Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков, а затем получите доступ к звуковому языку по отдельности с помощью индекса, основанного на единицах.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Аудиолангуажекаунт**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. Куррентаудиолангуаже**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. Куррентаудиолангуажеиндекс**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. Жетаудиолангуажеид**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. Жетлангуаженаме**](controls-getlanguagename.md)
</dt> </dl>

 

 





