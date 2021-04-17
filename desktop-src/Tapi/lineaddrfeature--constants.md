---
description: В \_ константах линеаддрфеатуре перечислены операции, которые могут быть вызваны по адресу.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Константы LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675541"
---
# <a name="lineaddrfeature_-constants"></a>\_Константы линеаддрфеатуре

В константах **линеаддрфеатуре \_** перечислены операции, которые могут быть вызваны по адресу.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**ЛИНЕАДДРФЕАТУРЕ \_ вперед**
</dt> <dd> <dl> <dt>



Адрес можно перенаправить.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**ЛИНЕАДДРФЕАТУРЕ \_ MAKECALL**
</dt> <dd> <dl> <dt>



Исходящий вызов может быть размещен по адресу.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**\_Отправка линеаддрфеатуре**
</dt> <dd> <dl> <dt>



Вызов можно получить по адресу.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупдирект**
</dt> <dd> <dl> <dt>



Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для получения вызова по определенному адресу.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупграуп**
</dt> <dd> <dl> <dt>



Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для выбора вызова в группе.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккуфелд**
</dt> <dd> <dl> <dt>



Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (с адресом назначения **null** ) можно использовать для получения вызова, который хранится по адресу. Обычно это используется только в расположении, исключающем мост.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупваитинг**
</dt> <dd> <dl> <dt>



Чтобы получить ожидающий вызов, можно использовать функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (с адресом назначения **null** ). Обратите внимание, что это не обязательно указывает на фактическое присутствие ожидающего вызова, поскольку для устройства телефонии часто бывает невозможно автоматически обнаружить такой вызов. Однако он указывает, что функция-ловушка будет вызываться для попытки переключения на такой вызов.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сетмедиаконтрол**
</dt> <dd> <dl> <dt>



Для этого адреса можно задать элемент управления мультимедиа.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сеттерминал**
</dt> <dd> <dl> <dt>



Можно задать режимы терминала для этого адреса.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сетупконф**
</dt> <dd> <dl> <dt>



В этом адресе можно настроить конференц-вызов с **нулевым** начальным вызовом.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**ЛИНЕАДДРФЕАТУРЕ \_ ункомплетекалл**
</dt> <dd> <dl> <dt>



Запросы на завершение вызовов могут быть отменены по этому адресу.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**\_НЕприпаркованный линеаддрфеатуре**
</dt> <dd> <dl> <dt>



Вызовы можно отменять с помощью этого адреса.

> [!Note]  
> Если в элементе **дваддрессфеатурес** в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) не задано ни одного нового измененного бита "раскладки", но \_ установлен бит раскладки линеаддрфеатуре, то любой из режимов подбора может работать; поставщик услуг просто не указал, какие из них.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**ЛИНЕАДДРФЕАТУРЕ \_ форвардднд**
</dt> <dd> <dl> <dt>



Функция [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (с пустым адресом назначения) может использоваться для включения функции "не беспокоить" в адресе. \_Также будет задано перенаправление линеаддрфеатуре.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**ЛИНЕАДДРФЕАТУРЕ \_ форвардфвд**
</dt> <dd> <dl> <dt>



Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) можно использовать для переадресации вызовов по адресу на другие числа. \_Также будет задано перенаправление линеаддрфеатуре.

> [!Note]  
> Если в элементе **дваддрессфеатурес** в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) не задан ни один из новых измененных бит пересылки, но установлен бит перенаправления линеаддрфеатуре \_ , то любой из режимов прямого доступа может работать; поставщик услуг просто не указал, какие из них.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Эта константа используется в [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (возвращается [**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) и в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (возвращается [**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **Линеаддресскапс** сообщает о доступности компонентов адреса поставщиком услуг (в основном коммутаторе) для заданного адреса. Приложение сделает это определение при инициализации. Структура [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) сообщает об определенном адресе, который может вызывать функции, пока адрес находится в текущем состоянии. Приложение сделает это определение динамически после изменения состояния адреса, как правило, вызванные действиями, связанными с вызовами по адресу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




