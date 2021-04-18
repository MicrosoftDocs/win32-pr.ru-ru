---
description: Указывает и настраивает службы, которые должны быть активными в домене службы, который был указан при вызове либо Кокреатеактивити, либо Коентерсервицедомаин.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Класс Ксервицеконфиг (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701177"
---
# <a name="cserviceconfig-class"></a>Класс Ксервицеконфиг

Указывает и настраивает службы, которые должны быть активными в домене службы, который был указан при вызове либо [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , либо [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID      | \_КСЕРВИЦЕКОНФИГ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ProgID:     | L "КОМСВКС. Ксервицеконфиг "                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Интерфейсы | [**исервицекомтиинтринсиксконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [**исервицеиисинтринсиксконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [**исервицеинхеританцеконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [**исервицепартитионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [**исервицескссконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [**исервицесинчронизатионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [**исервицесреадпулконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [**исервицетраккерконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [**исервицетрансактионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a>Назначение

Этот класс используется для настройки служб, которые необходимо использовать. [**Кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) и [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) позволяют использовать службы, настроенные этим классом, без необходимости привязывать эти службы к компоненту перед их использованием.

Этот класс не предназначен для использования в Visual Basic.

## <a name="remarks"></a>Комментарии

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Объекты, создаваемые из класса **ксервицеконфиг** , объединяют Свободный потоковый маршалеру, чтобы их можно было хранить в средах выполнения системы и повторно использовать в разных апартаментах.

Чтобы настроить отдельную службу, вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса, связанного со службой, а затем вызовите методы для этого интерфейса, чтобы установить соответствующую конфигурацию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[**кокреатефрисреадедмаршалер**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Службы COM+ без компонентов](com--services-without-components.md)
</dt> </dl>

 

