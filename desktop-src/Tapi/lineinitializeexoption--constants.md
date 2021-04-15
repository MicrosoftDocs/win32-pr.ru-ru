---
description: '\_Константы линеинитиализиксоптион указывают, какой механизм уведомления о событиях следует использовать при инициализации сеанса.'
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Константы LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689160"
---
# <a name="lineinitializeexoption_-constants"></a>\_Константы линеинитиализиксоптион

Константы **линеинитиализиксоптион \_** указывают, какой механизм уведомления о событиях следует использовать при инициализации сеанса.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ каллхубтраккинг**
</dt> <dd> <dl> <dt>



Приложение похочет использовать механизм уведомления о событии для отслеживания центра вызовов. Эта константа предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усекомплетионпорт**
</dt> <dd> <dl> <dt>



Приложение похочет использовать механизм уведомления о событиях порта завершения. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усивент**
</dt> <dd> <dl> <dt>



Приложение использует механизм уведомления о событиях обработчика событий. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**ЛИНЕИНИТИАЛИЗИКСОПТИОН \_ усехидденвиндов**
</dt> <dd> <dl> <dt>



Необходимо, чтобы приложение использовало механизм уведомления о событиях скрытого окна. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения о работе этих параметров см. в разделе [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




