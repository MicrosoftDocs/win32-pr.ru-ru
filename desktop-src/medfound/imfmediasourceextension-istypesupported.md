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
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693864"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




