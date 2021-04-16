---
description: '\_Константы побитового флага линегасертерм описывают условия, при которых сбор буферизованных цифр завершается.'
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Константы LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680031"
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

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




