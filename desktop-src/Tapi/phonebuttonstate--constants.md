---
description: Константы битовой флага ФОНЕБУТТОНСТАТЕ описывают позиции кнопок.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Константы PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689533"
---
# <a name="phonebuttonstate_-constants"></a>Константы PHONEBUTTONSTATE_

**PHONEBUTTONSTATE_** константы битовых флагов описывают позиции кнопки.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Кнопка находится в состоянии "вниз" (нажата вниз).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Указывает, что состояние кнопки не известно поставщику услуг и не будет известно в будущем. (TAPI версии 1,4 и более поздней)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Указывает, что состояние кнопки в данный момент неизвестно, но может быть известно в будущем. (TAPI версии 1,4 и более поздней)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Кнопка находится в состоянии "вверх".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API на телефоне и не использовать эти PHONEBUTTONSTATE_ значения, которые не поддерживает согласованная версия.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




