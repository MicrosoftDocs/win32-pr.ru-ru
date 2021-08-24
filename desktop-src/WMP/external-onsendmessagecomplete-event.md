---
title: Внешнее событие Онсендмессажекомплете
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Онсендмессажекомплете
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- проигрыватель Windows Media события External. онсендмессажекомплете
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dede59d2c52f20050a490e6ded1389e63884e598868e9736195280e3269a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648734"
---
# <a name="externalonsendmessagecomplete-event"></a>Внешнее событие Онсендмессажекомплете

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Событие **онсендмессажекомплете** возникает, когда Интернет-магазин завершил обработку сообщения. Сценарий на странице обнаружения ранее отправил сообщение путем вызова метода [External. SendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Возможные значения

это свойство только для записи, которое указывает имя функции в скрипте, проигрыватель Windows Media вызывается при возникновении события.

## <a name="parameters"></a>Параметры

Функция, обрабатывающая это событие, имеет следующие параметры.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Об*
</dt> <dd>

Та же строка, которая была передана в параметре **MSG** для **SendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Байт*
</dt> <dd>

Та же строка, которая была передана в параметре **param** для **SendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Результат*
</dt> <dd>

**Строка** , содержащая результат обработки сообщения. См. заметки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Метод **SendMessage** вызывает [Ивмпконтентпартнер:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), который возвращает асинхронно. То есть он возвращается до того, как Интернет-магазин завершит обработку сообщения. Когда Интернет-магазин заканчивает обработку сообщения, он вызывает [ивмпконтентпартнеркаллбакк:: сендмессажекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), который, в свою очередь, вызывает обработчик событий **онсендмессажекомплете** в скрипте.

Когда Интернет-магазин вызывает **ивмпконтентпартнеркаллбакк:: сендмессажекомплете**, он предоставляет код результата в параметре *бстрресулт* . проигрыватель Windows Media не интерпретирует этот код результата. вместо этого проигрыватель Windows Media передает код результата в обработчик событий **онсендмессажекомплете** в параметре *result* .

ни один из параметров (*Msg*, *Param*, *Result*) обработчика событий **онсендмессажекомплете** не интерпретируется проигрыватель Windows Media. Параметры имеют значение только в Интернет-магазине.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. sendMessage**](external-sendmessage.md)
</dt> <dt>

[**Ивмпконтентпартнер:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**Ивмпконтентпартнеркаллбакк:: Сендмессажекомплете**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





