---
title: Иконфигасфвритер Жеткуррентпрофилегуид, метод
description: Метод Жеткуррентпрофилегуид извлекает текущий GUID профиля системы Windows Media.
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
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338796"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Метод Иконфигасфвритер:: Жеткуррентпрофилегуид

Метод **жеткуррентпрофилегуид** ИЗВЛЕКАЕТ текущий GUID профиля системы Windows Media.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
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

## <a name="remarks"></a>Комментарии

Этот метод не используется с пользовательскими профилями (включая все профили, включающие потоки, использующие аудиокодеки Windows Media и видеокодеки), так как все такие профили создаются приложениями и не имеют идентификатора GUID. Если системный профиль не загружен, *ппрофилегуид* будет иметь **значение NULL**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 