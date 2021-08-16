---
description: '\_Константы битовой флага фонебуттонмоде описывают классы кнопок.'
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Константы PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761306"
---
# <a name="phonebuttonmode_-constants"></a>\_Константы фонебуттонмоде

Константы битовой флага **фонебуттонмоде \_** описывают классы кнопок.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_вызов фонебуттонмоде**
</dt> <dd> <dl> <dt>



Кнопке присваивается внешний вид вызова.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**ФОНЕБУТТОНМОДЕ \_ дисплей**
</dt> <dd> <dl> <dt>



Кнопка является «мягкой» кнопкой, связанной с дисплеем телефона. Набор телефонных номеров может содержать ноль или более экранных кнопок.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**ФОНЕБУТТОНМОДЕ \_ фиктивный**
</dt> <dd> <dl> <dt>



Это значение используется для описания расположения кнопки или лампы, не имеющей соответствующей кнопки, но имеющей только лампу.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_функция фонебуттонмоде**
</dt> <dd> <dl> <dt>



Кнопка назначается для запроса функций из коммутатора, например удержания, Конференции и перемещения.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**ФОНЕБУТТОНМОДЕая \_ клавиатура**
</dt> <dd> <dl> <dt>



Кнопка является одной из двенадцати кнопок клавиатуры, от 0 до 9, " \* " и " \# ".


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**ФОНЕБУТТОНМОДЕ \_ локальный**
</dt> <dd> <dl> <dt>



Кнопка является локальной функцией, такой как звук или регулятор громкости.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

Этот тип перечисления используется в структуре данных [**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) для описания значения, связанного с кнопками телефона.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




