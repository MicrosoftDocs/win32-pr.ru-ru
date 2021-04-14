---
description: 'Версия метода Имфконтентпротектионманажер:: Бегиненаблеконтент, поддерживающая удаленное взаимодействие.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: Ремотебегиненаблеконтент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647223"
---
# <a name="remotebeginenablecontent"></a>ремотебегиненаблеконтент

Версия метода [**имфконтентпротектионманажер:: бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Комментарии

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




