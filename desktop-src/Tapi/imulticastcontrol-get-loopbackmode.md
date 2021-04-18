---
description: Метод Get \_ лупбаккмоде получает режим многоадресного замыкания на себя.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Метод Имултикастконтрол:: get_LoopbackMode (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685432"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>Метод Имултикастконтрол:: Get \_ лупбаккмоде

\[**получить \_ Лупбаккмоде** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Get \_ лупбаккмоде** получает режим многоадресного замыкания на себя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмоде* \[ заполняет\]
</dt> <dd>

Указатель на дескриптор [**\_ \_ режима многоадресной рассылки**](multicast-loopback-mode.md) в текущем режиме замыкания на себя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Значение                                                                                        | Значение                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод успешно выполнен.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *пмоде* .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>Конфприв. h</dt> </dl> |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имултикастконтрол**](imulticastcontrol.md)
</dt> </dl>

 

 




