---
title: Иконфигасфвритер Конфигурефилтерусингпрофилеид, метод
description: Метод Конфигурефилтерусингпрофилеид настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля. (только для профилей Windows Media Format 4,0.)
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
ms.openlocfilehash: 6321d259a213426df7e4490c3fc8a793e583a6fcdf58ec795a9f88e43645377f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028488"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Метод Иконфигасфвритер:: Конфигурефилтерусингпрофилеид

Метод **конфигурефилтерусингпрофилеид** настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля. (только для профилей Windows Media Format 4,0.)

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

идентификатор профиля, определенный в версии 4,0 пакета SDK для Windows Media Format.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                         | Описание                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Метод выполнен успешно.<br/>        |
| <dl> <dt>**\_Ошибка E**</dt> </dl>              | Недопустимый профиль.<br/>    |
| <dl> <dt>**VFW \_ E — \_ неправильное \_ состояние**</dt> </dl> | Граф фильтра остановлен.<br/> |



 

## <a name="remarks"></a>Remarks

этот метод устарел, поскольку предполагается, что он имеет версию 4,0 Windows профили пакета SDK для формата носителя. Чтобы настроить фильтр для профилей версии 7,0 и более поздних, используйте [**иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) или [**Иконфигасфвритер:: конфигурефилтерусингпрофилегуид**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

