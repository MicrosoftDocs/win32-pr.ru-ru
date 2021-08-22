---
description: Возвращает состояние ошибки, связанное с сеансом ключа мультимедиа.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'Метод Имфмедиакэйсессион:: Error'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7698d059bd7d930037096208668de91292bca9e67b13743d353d3f682ec905a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357764"
---
# <a name="imfmediakeysessiongeterror-method"></a>Метод Имфмедиакэйсессион:: Error

Возвращает состояние ошибки, связанное с сеансом ключа мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*code* 
</dt> <dd>

Код ошибки.

</dd> <dt>

*системкоде* 
</dt> <dd>

Сведения об ошибках, специфичных для платформы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфмедиакэйсессион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




