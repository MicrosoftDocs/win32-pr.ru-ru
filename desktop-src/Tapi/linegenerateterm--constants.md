---
description: '\_Константы побитового флага линеженератетерм описывают условия, при которых заканчивается создание цифр или тона.'
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Константы LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c34d119f503c677e5c251bb494c5ea991dbd0fccf0bfbdb3affecf4c4ff1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518974"
---
# <a name="linegenerateterm_-constants"></a>\_Константы линеженератетерм

Константы побитового флага **линеженератетерм \_** описывают условия, при которых заканчивается создание цифр или тона.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**ЛИНЕЖЕНЕРАТЕТЕРМ \_ Отмена**
</dt> <dd> <dl> <dt>



Запрос на формирование цифр или тонов был отменен этим приложением, другим приложением или из-за прекращения вызова. Это значение также может быть возвращено, если не удается завершить создание цифр или тона из-за внутренней ошибки поставщика услуг.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**ЛИНЕЖЕНЕРАТЕТЕРМ \_ Готово**
</dt> <dd> <dl> <dt>



Запрошенное количество цифр или запрошенных тонов было создано в течение запрошенного времени.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




