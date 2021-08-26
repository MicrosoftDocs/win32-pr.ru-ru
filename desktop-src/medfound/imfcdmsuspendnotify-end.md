---
description: Будет выполнена фактическая приостановка, и в модуль расшифровки содержимого (CDM) больше не будут выполняться никакие вызовы.
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'Метод Имфкдмсуспенднотифи:: end'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9ad64b4b02c6accae3749478e09dee6078050bf22c0b1e5d13e4d1ea37f1635c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957914"
---
# <a name="imfcdmsuspendnotifyend-method"></a>Метод Имфкдмсуспенднотифи:: end

Будет выполнена фактическая приостановка, и в модуль расшифровки содержимого (CDM) больше не будут выполняться никакие вызовы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфкдмсуспенднотифи**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




