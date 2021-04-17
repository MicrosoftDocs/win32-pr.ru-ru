---
description: '\_Константы побитового флага линетрансфермоде описывают различные способы разрешения запросов на пересылку вызовов.'
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Константы LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674967"
---
# <a name="linetransfermode_-constants"></a>\_Константы линетрансфермоде

Константы побитового флага **линетрансфермоде \_** описывают различные способы разрешения запросов на пересылку вызовов.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_Конференция линетрансфермоде**
</dt> <dd> <dl> <dt>



Перенос разрешается путем создания односторонней конференции между приложением, стороной, подключенной к первому вызову, и стороной, подключенной к вызову консультации. При выборе этого параметра создается вызов Конференции.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_Перенос линетрансфермоде**
</dt> <dd> <dl> <dt>



Передача разрешается путем передачи начального вызова в вызов консультации. Оба вызова превращаются в состояние простоя приложения.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




