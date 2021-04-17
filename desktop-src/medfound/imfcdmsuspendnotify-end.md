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
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711789"
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
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфкдмсуспенднотифи**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




