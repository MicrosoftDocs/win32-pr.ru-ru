---
title: Иконфигасфвритер Жеткуррентпрофилеид, метод
description: Метод Жеткуррентпрофилеид извлекает идентификатор текущего профиля. (только для профилей Windows Media Format 4,0.)
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
ms.openlocfilehash: e065e15b0c73b4b1037003dee936af5f74208e4433c6925594e18ab92319028c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655479"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>Метод Иконфигасфвритер:: Жеткуррентпрофилеид

Метод **жеткуррентпрофилеид** извлекает идентификатор текущего профиля. (только для профилей Windows Media Format 4,0.)

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
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

## <a name="remarks"></a>Remarks

этот метод устарел, поскольку предполагается, что он имеет версию 4,0 Windows профили пакета SDK для формата носителя. Вместо этого используйте [**иконфигасфвритер:: жеткуррентпрофиле**](iconfigasfwriter-getcurrentprofile.md) или [**Иконфигасфвритер:: жеткуррентпрофилегуид**](iconfigasfwriter-getcurrentprofileguid.md) , чтобы правильно указать профиль для версии 7,0 и более поздних версий.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 