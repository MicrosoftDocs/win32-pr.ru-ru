---
title: Имстскаксевентс Онаусентикатионварнингдисмиссед, метод
description: вызывается после того, как элемент управления "ActiveX" отображает диалоговое окно проверки подлинности (например, диалоговое окно "ошибка сертификата").
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаусентикатионварнингдисмиссед
- Службы удаленных рабочих столов метода Онаусентикатионварнингдисмиссед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онаусентикатионварнингдисмиссед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a55af8450160e271e96c53d4d5a9d4390393ab7880d2c2bb143cf0e6a1cb3bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125234"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>Метод Имстскаксевентс:: Онаусентикатионварнингдисмиссед

вызывается после того, как элемент управления "ActiveX" отображает диалоговое окно проверки подлинности (например, диалоговое окно "ошибка сертификата").

## <a name="syntax"></a>Синтаксис


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

При необходимости можно использовать свойство [**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) для возврата всех родительских элементов, которые могли быть выполнены в методе [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows сервер 2008, Windows server 2008 с пакетом обновления 1<br/>                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





