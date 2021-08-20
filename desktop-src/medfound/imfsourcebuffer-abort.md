---
description: Прерывает обработку текущего сегмента мультимедиа.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'Метод Имфсаурцебуффер:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9cdce9e505940c4314871b82261dbc9ac199b800cda6e93f77a4eb967f83322c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062878"
---
# <a name="imfsourcebufferabort-method"></a>Метод Имфсаурцебуффер:: Abort

Прерывает обработку текущего сегмента мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Abort();
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



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




