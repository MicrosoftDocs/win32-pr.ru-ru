---
description: Задает продолжительность источника мультимедиа в 100-наносекундных единицах.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Метод Имфмедиасаурцеекстенсион:: Сетдуратион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061214"
---
# <a name="imfmediasourceextensionsetduration-method"></a>Метод Имфмедиасаурцеекстенсион:: Сетдуратион

Задает продолжительность источника мультимедиа в 100-наносекундных единицах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Длительность* \[ окне\]
</dt> <dd>

Длительность источника мультимедиа в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




