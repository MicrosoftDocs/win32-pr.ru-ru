---
title: Иконфигасфвритер Жеткуррентпрофиле, метод
description: Метод Жеткуррентпрофиле извлекает профиль, определяемый приложением.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Формат Windows Media, Жеткуррентпрофиле метод
- Жеткуррентпрофиле метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофиле
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198385"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Метод Иконфигасфвритер:: Жеткуррентпрофиле

Метод **жеткуррентпрофиле** извлекает профиль, определяемый приложением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пппрофиле* \[ заполняет\]
</dt> <dd>

Адрес указателя, получающего интерфейс [**ивмпрофиле**](iwmprofile.md) определяемого приложением профиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если метод завершается успешно, возвращаемый им указатель **ивмпрофиле** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 