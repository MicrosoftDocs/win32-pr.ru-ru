---
description: Закрывает сеанс ключа мультимедиа и должен вызываться перед освобождением сеанса ключа.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Метод Имфмедиакэйсессион:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: f172f88f0e13acd3d44f673e5a142fafe9f7075677d8496b5332af0607e89846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062993"
---
# <a name="imfmediakeysessionclose-method"></a>Метод Имфмедиакэйсессион:: Close

Закрывает сеанс ключа мультимедиа и должен вызываться перед освобождением сеанса ключа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Close();
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

[**имфмедиакэйсессион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




