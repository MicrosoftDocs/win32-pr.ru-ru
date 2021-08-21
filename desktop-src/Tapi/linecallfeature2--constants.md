---
description: В \_ списке константы LINECALLFEATURE2 перечислены дополнительные функции, доступные для конференций, передачи и вызовов парковки.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Константы LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b1ef95c5427c70455466fdc4e44424a8d7bc92f768698bd3356f28256b4dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003142"
---
# <a name="linecallfeature2_-constants"></a>\_Константы LINECALLFEATURE2

В списке константы **LINECALLFEATURE2 \_** перечислены дополнительные функции, доступные для конференций, передачи и вызовов парковки.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ комплкаллбакк**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию обратного вызова можно вызвать с помощью \_ параметра обратного вызова линекомплмоде с [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Бит ЛИНЕКАЛЛФЕАТУРЕ \_ COMPLETECALL также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ комплкампон**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию "Camp on" можно вызвать с помощью \_ параметра линекомплмоде кампон с [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Бит ЛИНЕКАЛЛФЕАТУРЕ \_ COMPLETECALL также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ комплинтруде**
</dt> <dd> <dl> <dt>



Если этот бит включен, функция "атака" может быть вызвана с помощью параметра "ЛИНЕКОМПЛМОДЕная \_ атака" с [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Бит ЛИНЕКАЛЛФЕАТУРЕ \_ COMPLETECALL также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ комплмессаже**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию "выйти из сообщения" можно вызвать с помощью \_ параметра сообщения линекомплмоде с [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Бит ЛИНЕКАЛЛФЕАТУРЕ \_ COMPLETECALL также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ нохолдконференце**
</dt> <dd> <dl> <dt>



Если этот бит включен, то с помощью \_ параметра линекаллпарамфлагс нохолдконференце с [**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)можно создать "без удержания". Бит ЛИНЕКАЛЛФЕАТУРЕ \_ сетупконф также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ онестептрансфер**
</dt> <dd> <dl> <dt>



Если этот бит включен, то можно создать "один шаг для перемещения" с помощью параметра ЛИНЕКАЛЛПАРАМФЛАГС \_ онестептрансфер с [**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Бит ЛИНЕКАЛЛФЕАТУРЕ \_ сетуптрансфер также будет включен в член **двкаллфеатурес** .

> [!Note]  
> Если в элементе **dwCallFeatures2** в [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) не указан ни один из битов "Comp", но указан линекаллфеатуре \_ COMPLETECALL, то возможно, что любой из них будет работать, но поставщик услуг не указал, какой.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ трансферконф**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию [**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) можно использовать для разрешения перемещения в качестве односторонней Конференции. Бит ЛИНЕКАЛЛФЕАТУРЕ \_ комплететрансф также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ трансфернорм**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию [**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) можно использовать для разрешения перемещения в качестве обычного перемещения. Бит ЛИНЕКАЛЛФЕАТУРЕ \_ комплететрансф также будет включен в член **двкаллфеатурес** .

> [!Note]  
> Если ни ТРАНСФЕРНОРМ, ни ТРАНСФЕРКОНФ не указаны в элементе **dwCallFeatures2** в [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , но \_ указано линекаллфеатуре комплететрансф, то возможно, что либо будет работать, но поставщик услуг не указал, какой.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ паркдирект**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию "направленный приостановку" можно вызвать с помощью \_ параметра линепаркмоде directed WITH [**линепарк**](/windows/desktop/api/Tapi/nf-tapi-linepark). \_Бит парковки линекаллфеатуре также будет включен в член **двкаллфеатурес** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ паркнондирект**
</dt> <dd> <dl> <dt>



Если этот бит включен, функцию "ненаправленный приостановку" можно вызвать с помощью параметра ЛИНЕПАРКМОДЕ ненаправленный \_ с [**линепарк**](/windows/desktop/api/Tapi/nf-tapi-linepark). \_Бит парковки линекаллфеатуре также будет включен в член **двкаллфеатурес** .

> [!Note]  
> Если ни ПАРКДИРЕКТ, ни ПАРКНОНДИРЕКТ не указаны в элементе **dwCallFeatures2** в [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , но \_ указано линекаллфеатуре парковки, то возможно, что либо будет работать, но поставщик услуг не указал, какой.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**линепарк**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




