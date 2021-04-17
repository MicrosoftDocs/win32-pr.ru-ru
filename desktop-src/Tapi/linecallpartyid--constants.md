---
description: '\_Константы побитового флага линекаллпартид описывают характер доступной информации о сторонах, вовлеченных в вызов.'
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Константы LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689388"
---
# <a name="linecallpartyid_-constants"></a>\_Константы линекаллпартид

Константы побитового флага **линекаллпартид \_** описывают характер доступной информации о сторонах, вовлеченных в вызов.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**ЛИНЕКАЛЛПАРТИД \_ адрес**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта состоят из адреса субъекта в каноническом формате адреса или в формате коммутируемого адреса.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**ЛИНЕКАЛЛПАРТИД \_ заблокирована**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта недоступны, так как они заблокированы удаленной стороной.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**\_имя линекаллпартид**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта состоят из имени стороны (например, из каталога, который хранится внутри коммутатора).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**ЛИНЕКАЛЛПАРТИД \_ аутофареа**
</dt> <dd> <dl> <dt>



Сведения об ИДЕНТИФИКАТОРе вызывающего объекта недоступны, так как они не распространяются по сети.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**ЛИНЕКАЛЛПАРТИД \_ частичный**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта допустимы, но ограничены только частичными сведениями.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**ЛИНЕКАЛЛПАРТИД \_ НЕсвободно**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта недоступны и станут недоступны позже. Сведения могут быть недоступны по неопределенным причинам. Например, информация не была доставлена сетью, она была пропущена поставщиком услуг и т. д.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**ЛИНЕКАЛЛПАРТИД \_ неизвестный**
</dt> <dd> <dl> <dt>



Сведения об идентификаторе субъекта в настоящее время неизвестны, но могут быть известны позже.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Для каждой из возможных сторон, участвующих в вызове, константы **линекаллпартид \_** описывают форматирование сведений об идентификаторе субъекта. Эта информация предоставляется в структуре данных [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




