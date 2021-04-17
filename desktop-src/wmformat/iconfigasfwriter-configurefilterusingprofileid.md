---
title: Иконфигасфвритер Конфигурефилтерусингпрофилеид, метод
description: Метод Конфигурефилтерусингпрофилеид настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля. (Только для профилей Windows Media формата 4,0.)
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Формат Windows Media, Конфигурефилтерусингпрофилеид метод
- Конфигурефилтерусингпрофилеид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Конфигурефилтерусингпрофилеид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710304"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Метод Иконфигасфвритер:: Конфигурефилтерусингпрофилеид

Метод **конфигурефилтерусингпрофилеид** настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля. (Только для профилей Windows Media формата 4,0.)

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпрофилеид* \[ окне\]
</dt> <dd>

Идентификатор профиля, определенный в версии 4,0 пакета SDK Windows Media Format.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                         | Описание                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Метод выполнен успешно.<br/>        |
| <dl> <dt>**\_Ошибка E**</dt> </dl>              | Недопустимый профиль.<br/>    |
| <dl> <dt>**VFW \_ E — \_ неправильное \_ состояние**</dt> </dl> | Граф фильтра остановлен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод устарел, так как в нем предполагается наличие профилей пакета SDK для формата Windows Media версии 4,0. Чтобы настроить фильтр для профилей версии 7,0 и более поздних, используйте [**иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) или [**Иконфигасфвритер:: конфигурефилтерусингпрофилегуид**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

