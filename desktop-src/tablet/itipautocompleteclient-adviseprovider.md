---
description: Регистрирует поставщик в клиенте, чтобы позволить клиенту вызывать объект поставщика автозавершения приложения.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Метод Итипаутокомплетеклиент:: Адвисепровидер (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dd48cdfbf35c5132b42f8185cdc93f53ec34c77df78a51d16da9fa5a5311c144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938584"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>Метод Итипаутокомплетеклиент:: Адвисепровидер

Регистрирует поставщик в клиенте, чтобы позволить клиенту вызывать объект поставщика автозавершения приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндфиелд* \[ окне\]
</dt> <dd>

Описатель окна поля, предоставляющего функцию автозавершения.

</dd> <dt>

*пиакпровидер* \[ окне\]
</dt> <dd>

Указатель интерфейса на интерфейс автоматического завершения поставщика.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                       |
| Заголовок<br/>                   | <dl> <dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Итипаутокомплетеклиент**](itipautocompleteclient.md)
</dt> <dt>

[**Метод Итипаутокомплетеклиент:: Унадвисепровидер**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Справочник по панели ввода текста](text-input-panel-reference.md)
</dt> </dl>

 

 




