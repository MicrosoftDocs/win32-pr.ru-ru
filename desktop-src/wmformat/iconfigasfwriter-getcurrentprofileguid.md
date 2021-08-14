---
title: Иконфигасфвритер Жеткуррентпрофилегуид, метод
description: метод жеткуррентпрофилегуид извлекает текущий идентификатор GUID профиля системы носителя Windows.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Формат Windows Media, Жеткуррентпрофилегуид метод
- Жеткуррентпрофилегуид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофилегуид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433643"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Метод Иконфигасфвритер:: Жеткуррентпрофилегуид

метод **жеткуррентпрофилегуид** извлекает текущий идентификатор GUID профиля системы носителя Windows.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппрофилегуид* \[ заполняет\]
</dt> <dd>

Указатель на переменную типа **GUID** , определяющую текущий системный профиль, используемый фильтром.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

этот метод не используется с пользовательскими профилями (включая все профили, которые включают потоки, использующие видеокодеки Windows Media), так как все такие профили создаются приложениями и не имеют идентификатора GUID. Если системный профиль не загружен, *ппрофилегуид* будет иметь **значение NULL**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 