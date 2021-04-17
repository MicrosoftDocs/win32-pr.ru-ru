---
title: Внешний метод проверки подлинности
description: Метод проверки подлинности инициирует попытку проверки подлинности пользователя.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- метод проверки подлинности Windows Media Player
- метод проверки подлинности Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод проверки подлинности
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695064"
---
# <a name="externalauthenticate-method"></a>Внешний метод проверки подлинности

Метод **проверки подлинности** инициирует попытку проверки подлинности пользователя.

## <a name="syntax"></a>Синтаксис


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аусентикатиониндекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), указывающее индекс веб-страницы успешного выполнения проверки подлинности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Некоторые ссылки на странице обнаружения имеют целевые объекты, которые должны отображаться только после проверки подлинности пользователя. На странице Обнаружение, проигрыватель Windows Media и подключаемый модуль интернет-магазина выполните следующие действия, чтобы проверить подлинность пользователя и отобразить целевую веб-страницу:

1.  Скрипт на странице обнаружения вызывает *внешний* объект. метод **проверки подлинности** .
2.  Проигрыватель Windows Media отображает диалоговое окно для получения имени пользователя и пароля.
3.  Проигрыватель Windows Media вызывает метод [ивмпконтентпартнер:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), который инициирует попытку проверки подлинности и немедленно возвращает результат.
4.  По завершении проверки подлинности подключаемый модуль интернет-магазина вызывает [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), передает Вмпкнаусресулт и логическое значение, указывающее, была ли попытка успешной.
5.  Если попытка проверки подлинности прошла успешно, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), передавая g \_ сзитеминфо \_ аусентикатионсукцессурл, чтобы получить URL-адрес веб-страницы, которая успешно проходит проверку подлинности. В этом вызове проигрыватель Windows Media передает тот же индекс, что и страница обнаружения, передаваемая *внешней*. метод **проверки подлинности** .
6.  Проигрыватель Windows Media отображает веб-страницу Проверка подлинности — успешно выполненная.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Аттемптлогин**](external-attemptlogin.md)
</dt> <dt>

[**External. Усерлогжедин**](external-userloggedin.md)
</dt> </dl>

 

 





