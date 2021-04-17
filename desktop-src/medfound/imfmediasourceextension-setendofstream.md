---
description: Указывает, что достигнут конец потока мультимедиа.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Метод Имфмедиасаурцеекстенсион:: Сетендофстреам'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713279"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>Метод Имфмедиасаурцеекстенсион:: Сетендофстреам

Указывает, что достигнут конец потока мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ошибка при* \[ окне\]
</dt> <dd>

Используется для передачи сведений об ошибках.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[**MF \_ , \_ Ошибка MSE**](mf-mse-error.md)
</dt> </dl>

 

 




