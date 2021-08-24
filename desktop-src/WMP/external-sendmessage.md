---
title: External. sendMessage, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод sendMessage отправляет сообщение подключаемому модулю Интернет-магазина.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- метод sendMessage проигрыватель Windows Media
- метод sendMessage проигрыватель Windows Media, внешний класс
- внешний класс проигрыватель Windows Media, метод sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648365"
---
# <a name="externalsendmessage-method"></a>External. sendMessage, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **SendMessage** отправляет сообщение подключаемому модулю Интернет-магазина.

## <a name="syntax"></a>Синтаксис


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сообщение* \[ окне\]
</dt> <dd>

**Строка** , содержащая сообщение.

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

**Строка** , содержащая параметры, связанные с сообщением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Сообщение отправляется асинхронно. Это значит, что этот метод возвращает значение немедленно, а не ожидает обработки сообщения. Когда подключаемый модуль заканчивает обработку сообщения, он вызывает метод [ивмпконтентпартнеркаллбакк:: сендмессажекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , который, в свою очередь, вызывает обработчик событий [онсендмессажекомплете](external-onsendmessagecomplete-event.md) в скрипте.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Онсендмессажекомплете**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**Ивмпконтентпартнер:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**Ивмпконтентпартнеркаллбакк:: Сендмессажекомплете**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





