---
description: '\_Константы побитового флага линегасертерм описывают условия, при которых сбор буферизованных цифр завершается.'
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Константы LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a6d5952ac4f69d11fd499df63554d6fda7dca76e46e4aad1a01ae326f363a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140037"
---
# <a name="linegatherterm_-constants"></a>\_Константы линегасертерм

Константы побитового флага **линегасертерм \_** описывают условия, при которых сбор буферизованных цифр завершается.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**ЛИНЕГАСЕРТЕРМ \_ буфферфулл**
</dt> <dd> <dl> <dt>



Было собрано запрошенное количество цифр. Буфер заполнен.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**ЛИНЕГАСЕРТЕРМ \_ Отмена**
</dt> <dd> <dl> <dt>



Запрос был отменен этим приложением, другим приложением или из-за прекращения вызова.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**ЛИНЕГАСЕРТЕРМ \_ фирсттимеаут**
</dt> <dd> <dl> <dt>



Истекло время ожидания первой цифры. Буфер не содержит цифр.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**ЛИНЕГАСЕРТЕРМ \_**
</dt> <dd> <dl> <dt>



Время ожидания между цифрами истекло. Буфер содержит по крайней мере одну цифру.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**ЛИНЕГАСЕРТЕРМ \_ термдигит**
</dt> <dd> <dl> <dt>



Одна из цифр завершения соответствует полученной цифре. Сопоставленная конечная цифра — это последняя цифра в буфере.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




