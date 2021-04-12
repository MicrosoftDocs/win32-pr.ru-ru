---
title: Имстскаксевентс Онаусентикатионварнингдисмиссед, метод
description: Вызывается после того, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").
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
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415456"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>Метод Имстскаксевентс:: Онаусентикатионварнингдисмиссед

Вызывается после того, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").

## <a name="syntax"></a>Синтаксис


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

При необходимости можно использовать свойство [**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) для возврата всех родительских элементов, которые могли быть выполнены в методе [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008, Windows Server 2008 с пакетом обновления 1<br/>                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





