---
title: Иконфигасфвритер Конфигурефилтерусингпрофилегуид, метод
description: Метод Конфигурефилтерусингпрофилегуид настраивает фильтр для записи файла ASF на основе указанного заранее заданного профиля. (Не рекомендуется.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Формат Windows Media, Конфигурефилтерусингпрофилегуид метод
- Конфигурефилтерусингпрофилегуид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Конфигурефилтерусингпрофилегуид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533410"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Метод Иконфигасфвритер:: Конфигурефилтерусингпрофилегуид

Метод **конфигурефилтерусингпрофилегуид** настраивает фильтр для записи файла ASF на основе указанного заранее заданного профиля. (Не рекомендуется.)

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*гуидпрофиле* \[ окне\]
</dt> <dd>

**Идентификатор GUID** , определяющий профиль, как определено в файле заголовка пакета SDK для формата Windows Media вмсиспрф. h.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                         | Описание                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Метод выполнен успешно.<br/>        |
| <dl> <dt>**\_Ошибка E**</dt> </dl>              | Недопустимый профиль.<br/>    |
| <dl> <dt>**VFW \_ E — \_ неправильное \_ состояние**</dt> </dl> | Граф фильтра остановлен.<br/> |



 

## <a name="remarks"></a>Комментарии

Начиная с Windows Media Format SDK серии 9 не были определены новые профили системы. С этим методом можно использовать только идентификаторы GUID системного профиля версии 8 (или более ранней).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

