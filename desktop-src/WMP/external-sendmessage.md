---
title: External. sendMessage, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод sendMessage отправляет сообщение подключаемому модулю Интернет-магазина.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- sendMessage, метод Windows Media Player
- sendMessage метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод sendMessage
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
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695063"
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

## <a name="remarks"></a>Комментарии

Сообщение отправляется асинхронно. Это значит, что этот метод возвращает значение немедленно, а не ожидает обработки сообщения. Когда подключаемый модуль заканчивает обработку сообщения, он вызывает метод [ивмпконтентпартнеркаллбакк:: сендмессажекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , который, в свою очередь, вызывает обработчик событий [онсендмессажекомплете](external-onsendmessagecomplete-event.md) в скрипте.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Онсендмессажекомплете**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**Ивмпконтентпартнер:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**Ивмпконтентпартнеркаллбакк:: Сендмессажекомплете**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





