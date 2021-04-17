---
description: '\_Константы побитового флага фонехуксвитчдев описывают различные устройства ввода-вывода с собственной хуксвитч, управляемой с компьютера.'
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Константы PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680105"
---
# <a name="phonehookswitchdev_-constants"></a>\_Константы фонехуксвитчдев

Константы побитового флага **фонехуксвитчдев \_** описывают различные устройства ввода-вывода с собственной хуксвитч, управляемой с компьютера.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**ФОНЕХУКСВИТЧДЕВная \_ трубка**
</dt> <dd> <dl> <dt>



Это Стандартный и мауспиеценый телефон.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**ФОНЕХУКСВИТЧДЕВ \_ гарнитура**
</dt> <dd> <dl> <dt>



Это гарнитура, подключенная к набору телефонов.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**ФОНЕХУКСВИТЧДЕВ \_ докладчик**
</dt> <dd> <dl> <dt>



Это встроенная громкоговоритель и микрофон. Это может быть также внешний подключенный к дополнения динамик с внешним подключением к телефонному набору.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Эти константы используются в структуре данных [**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) для указания возможностей устройства хуксвитч телефонного устройства. Структура [**фонестатус**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) сообщает о состоянии устройств хуксвитч телефона. Функция [**фонесесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) и [**фонежесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) используют ее в качестве параметра для выбора устройства ввода-вывода телефона.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




