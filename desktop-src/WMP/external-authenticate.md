---
title: Внешний метод проверки подлинности
description: Метод проверки подлинности инициирует попытку проверки подлинности пользователя.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- проигрыватель Windows Media метода проверки подлинности
- метод проверки подлинности проигрыватель Windows Media, внешний класс
- внешний класс проигрыватель Windows Media, метод проверки подлинности
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
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649554"
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

## <a name="remarks"></a>Remarks

Некоторые ссылки на странице обнаружения имеют целевые объекты, которые должны отображаться только после проверки подлинности пользователя. на странице обнаружение, проигрыватель Windows Media и подключаемом модуле интернет-магазина выполните следующие действия, чтобы проверить подлинность пользователя и отобразить целевую веб-страницу:

1.  Скрипт на странице обнаружения вызывает *внешний* объект. метод **проверки подлинности** .
2.  проигрыватель Windows Media отображает диалоговое окно для получения имени пользователя и пароля.
3.  проигрыватель Windows Media вызывает метод [ивмпконтентпартнер:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), который инициирует попытку проверки подлинности и немедленно возвращает значение.
4.  По завершении проверки подлинности подключаемый модуль интернет-магазина вызывает [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), передает Вмпкнаусресулт и логическое значение, указывающее, была ли попытка успешной.
5.  если попытка проверки подлинности прошла успешно, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), передавая g \_ сзитеминфо \_ аусентикатионсукцессурл, для получения URL-адреса веб-страницы с проверкой подлинности. в этом вызове проигрыватель Windows Media передает тот же индекс, что и страница обнаружения, передаваемая *внешней*. метод **проверки подлинности** .
6.  проигрыватель Windows Media отображает веб-страницу проверка подлинности — успешно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Аттемптлогин**](external-attemptlogin.md)
</dt> <dt>

[**External. Усерлогжедин**](external-userloggedin.md)
</dt> </dl>

 

 





