---
title: Метод remove_ConnectionStatusChanged Ибасикдевице
description: Отменяет регистрацию обработчика событий для события Коннектионстатусчанжед. | Метод remove_ConnectionStatusChanged Ибасикдевице
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API потоковой передачи мультимедиа remove_ConnectionStatusChanged метода
- API потоковой передачи remove_ConnectionStatusChanged метода, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703587"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Метод Ибасикдевице:: Remove \_ коннектионстатусчанжед

Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*токен* \[ окне\]
</dt> <dd>

Ссылка на маркер, полученный из метода [**Add \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md) при регистрации обработчика событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибасикдевице**](ibasicdevice.md)
</dt> </dl>

 

 





