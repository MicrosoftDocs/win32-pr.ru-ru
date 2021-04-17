---
description: '\_Константа битового флага линетранслатеоптион описывает параметр, используемый при преобразовании адресов.'
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Константы LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685445"
---
# <a name="linetranslateoption_-constants"></a>\_Константы линетранслатеоптион

Константа битового флага **линетранслатеоптион \_** описывает параметр, используемый при преобразовании адресов.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ канцелкаллваитинг**
</dt> <dd> <dl> <dt>



Если для расположения определена ожидающая строка вызова Cancel, установка этого бита приведет к вставке строки в начало строки с набором. Обычно это используется приложениями для работы с данными и модемами, чтобы предотвратить прерывание вызовов с помощью сигналов, ожидающих звонка. Если для расположения не определена ожидающая строка вызова Cancel, этот бит не влияет на. Обратите внимание, что в приложениях, использующих этот бит, рекомендуется также установить \_ Безопасный бит линекаллпарамфлагс в члене **Двкаллпарамфлагс** структуры [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , передаваемой в [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) с помощью параметра *лпкаллпарамс* . Таким образом, если линейное устройство использует механизм, отличный от цифр, доступных для набора, для подавления прерываний вызова этот механизм будет вызван.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ кардоверриде**
</dt> <dd> <dl> <dt>



Вызывающая карточка по умолчанию должна быть переопределена указанной.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ форцелд**
</dt> <dd> <dl> <dt>



Этот параметр приводит к тому, что адрес (номер) будет преобразован на длинное расстояние.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ форцелокал**
</dt> <dd> <dl> <dt>



Этот параметр задает принудительное преобразование числа (адреса) в локальную.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**линетранслатеаутпут**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




