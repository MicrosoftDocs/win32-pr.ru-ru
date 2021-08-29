---
description: Сообщение TAPI LINE \_ аддрессстате отправляется при изменении состояния адреса в строке, открытой в настоящий момент приложением. Приложение может вызвать Линежетаддрессстатус, чтобы определить текущее состояние адреса.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Сообщение LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfc158bd41b635142252546fbc289ed868851a3ac79d80bddba2df6118715bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959884"
---
# <a name="line_addressstate-message"></a>Строка \_ сообщения аддрессстате

Сообщение TAPI **Line \_ аддрессстате** отправляется при изменении состояния адреса в строке, открытой в настоящий момент приложением. Приложение может вызвать [**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) , чтобы определить текущее состояние адреса.


```C++
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер устройства линии.

</dd> <dt>

*двкаллбаккинстанце* 
</dt> <dd>

Экземпляр обратного вызова, указанный при открытии строки.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Идентификатор адреса, который изменил состояние.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Состояние адреса, которое было изменено. Может быть одной или несколькими [**\_ константами линеаддрессстате**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Сообщение **Line \_ аддрессстате** отправляется в любое приложение, которое открыло это устройство и включило это сообщение. Отправка этого сообщения для различных элементов состояния может контролироваться и запрашиваться с помощью [**линежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) и [**линесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). По умолчанию отчеты о состоянии адреса отключены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**линежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**линесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




