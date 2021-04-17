---
description: Создает объект сеанса ключа мультимедиа, используя указанные данные инициализации и пользовательские данные. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Метод Имфмедиакэйс:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693873"
---
# <a name="imfmediakeyscreatesession-method"></a>Метод Имфмедиакэйс:: CreateSession

Создает объект сеанса ключа мультимедиа, используя указанные данные инициализации и пользовательские данные. .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Успешности* 
</dt> <dd>

Тип MIME контейнера мультимедиа, используемого для содержимого.

</dd> <dt>

*initData* 
</dt> <dd>

Данные инициализации для системы ключей.

</dd> <dt>

*CB* 
</dt> <dd>

Число в байтах *initdata*.

</dd> <dt>

*Пользовательские* 
</dt> <dd>

Пользовательские данные, отправляемые в систему ключей.

</dd> <dt>

*кбкустомдата* 
</dt> <dd>

Число в байтах *кбкустомдата*.

</dd> <dt>

*явлении* 
</dt> <dd>

явлении

</dd> <dt>

*ппсессион* 
</dt> <dd>

Сеанс ключа мультимедиа.

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

[**имфмедиакэйс**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




