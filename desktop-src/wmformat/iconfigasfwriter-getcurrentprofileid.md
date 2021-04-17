---
title: Иконфигасфвритер Жеткуррентпрофилеид, метод
description: Метод Жеткуррентпрофилеид извлекает идентификатор текущего профиля. (Только для профилей Windows Media формата 4,0.)
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Формат Windows Media, Жеткуррентпрофилеид метод
- Жеткуррентпрофилеид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофилеид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691564"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>Метод Иконфигасфвритер:: Жеткуррентпрофилеид

Метод **жеткуррентпрофилеид** извлекает идентификатор текущего профиля. (Только для профилей Windows Media формата 4,0.)

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдвпрофилеид* \[ заполняет\]
</dt> <dd>

Указатель на переменную типа **DWORD** , которая получает идентификатор текущего профиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод устарел, так как в нем предполагается наличие профилей пакета SDK для формата Windows Media версии 4,0. Вместо этого используйте [**иконфигасфвритер:: жеткуррентпрофиле**](iconfigasfwriter-getcurrentprofile.md) или [**Иконфигасфвритер:: жеткуррентпрофилегуид**](iconfigasfwriter-getcurrentprofileguid.md) , чтобы правильно указать профиль для версии 7,0 и более поздних версий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 