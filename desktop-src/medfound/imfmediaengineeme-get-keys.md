---
description: Возвращает объект ключей мультимедиа, связанный с обработчиком мультимедиа, или значение null, если отсутствует объект ключей мультимедиа.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Метод Имфмедиаенгиниме:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713296"
---
# <a name="imfmediaengineemeget_keys-method"></a>Метод Имфмедиаенгиниме:: Get \_ Keys

Возвращает объект ключей мультимедиа, связанный с обработчиком мультимедиа, или **значение NULL** , если отсутствует объект ключей мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* 
</dt> <dd>

Объект ключей мультимедиа, связанный с обработчиком мультимедиа, или **значение NULL** , если отсутствует объект ключей мультимедиа.

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

[**имфмедиаенгиниме**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




