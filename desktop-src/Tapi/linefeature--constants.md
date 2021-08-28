---
description: '\_Константы линефеатуре список операций, которые могут быть вызваны в строке с помощью этого API.'
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Константы LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1d65ea846ea8209850837877e1e880fc89fed0ad7e0d6209b38ff0f3703f34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073054"
---
# <a name="linefeature_-constants"></a>\_Константы линефеатуре

**\_ Константы линефеатуре** список операций, которые могут быть вызваны в строке с помощью этого API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**ЛИНЕФЕАТУРЕ \_ девспеЦифик**
</dt> <dd> <dl> <dt>



В строке можно использовать операции для конкретных устройств.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**ЛИНЕФЕАТУРЕ \_ девспеЦификфеат**
</dt> <dd> <dl> <dt>



В строке можно использовать функции для конкретных устройств.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**ЛИНЕФЕАТУРЕ \_ вперед**
</dt> <dd> <dl> <dt>



В строке можно использовать пересылку всех адресов.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**ЛИНЕФЕАТУРЕ \_ форвардднд**
</dt> <dd> <dl> <dt>



Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (с пустым адресом назначения) можно использовать, чтобы включить функцию "не беспокоить" для всех адресов в строке. \_Также будет задано перенаправление линефеатуре. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**ЛИНЕФЕАТУРЕ \_ форвардфвд**
</dt> <dd> <dl> <dt>



Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) можно использовать для переадресации вызовов по всем адресам в строке на другие числа. \_Также будет задано перенаправление линефеатуре. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**ЛИНЕФЕАТУРЕ \_ MAKECALL**
</dt> <dd> <dl> <dt>



Исходящий вызов может быть размещен в этой строке с использованием неопределенного адреса.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**ЛИНЕФЕАТУРЕ \_ сетдевстатус**
</dt> <dd> <dl> <dt>



Функция [**линесетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) может быть вызвана на устройстве линии. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**ЛИНЕФЕАТУРЕ \_ сетмедиаконтрол**
</dt> <dd> <dl> <dt>



В этой строке можно задать элемент управления мультимедиа.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**ЛИНЕФЕАТУРЕ \_ сеттерминал**
</dt> <dd> <dl> <dt>



Можно задать режимы терминала для этой строки.

> [!Note]  
> Если в элементе **двлинефеатурес** в [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) не задан ни один из новых измененных бит пересылки, но установлен бит перенаправления линефеатуре \_ , то любой из режимов прямого доступа может работать; поставщик услуг просто не указал, какие из них.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

\_Константы линефеатуре используются в [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (возвращается [**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)). [**Линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) отчеты для определенной строки, какие функции строк фактически вызываются, пока строка находится в текущем состоянии. Приложение сделает это определение динамически после изменения состояния строки, как правило, из-за адреса или действий, связанных с вызовами, в строке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**линесетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




