---
description: '\_Сообщение АЖЕНТСПЕЦИФИК линии TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение. Приложение может вызвать Линежетажентстатус, чтобы определить текущее состояние агента.'
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Сообщение LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867164"
---
# <a name="line_agentspecific-message"></a>Строка \_ сообщения ажентспеЦифик

Сообщение **\_ АЖЕНТСПЕЦИФИК линии** TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение. Приложение может вызвать [**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) , чтобы определить текущее состояние агента.


```C++
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер приложения для линейного устройства.

</dd> <dt>

*двкаллбаккинстанце* 
</dt> <dd>

Экземпляр обратного вызова, указанный при открытии линии вызова.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Индекс в массиве идентификаторов расширения обработчика в структуре [**линеаженткапс**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) расширения обработчика, с которым связано сообщение.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Относится к расширению обработчика. Как правило, это значение используется, чтобы приложение вызывало функцию [**линеажентспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) для получения дополнительных сведений о сообщении.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Относится к расширению обработчика.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

**Строка \_ ажентспеЦифик** сообщения не отправляется в приложения, поддерживающие более старые версии TAPI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**линеаженткапс**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**линеажентспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




