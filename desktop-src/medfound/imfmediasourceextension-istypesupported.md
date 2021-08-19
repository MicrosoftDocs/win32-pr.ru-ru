---
description: Возвращает значение, указывающее, поддерживается ли указанный тип MIME источником мультимедиа.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Метод Имфмедиасаурцеекстенсион:: Истипесуппортед'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974343"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>Метод Имфмедиасаурцеекстенсион:: Истипесуппортед

Возвращает значение, указывающее, поддерживается ли указанный тип MIME источником мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тип* \[ окне\]
</dt> <dd>

Тип носителя для проверки поддержки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**значение true** , если тип мультимедиа поддерживается; в противном случае — **значение false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




