---
title: Имстскаксевентс Онаусентикатионварнингдисплайед, метод
description: вызывается перед тем, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "ошибка сертификата").
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаусентикатионварнингдисплайед
- Службы удаленных рабочих столов метода Онаусентикатионварнингдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онаусентикатионварнингдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854012"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>Метод Имстскаксевентс:: Онаусентикатионварнингдисплайед

вызывается перед тем, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "ошибка сертификата").

## <a name="syntax"></a>Синтаксис


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

При необходимости можно использовать свойство [**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) , чтобы убедиться, что модальное диалоговое окно проверки подлинности будет дочерним по отношению к указанному окну (это может потребоваться, чтобы запретить пользователям использовать другие диалоговые окна во время отображения диалогового окна проверки подлинности). по умолчанию родительским элементом является окно управления ActiveX.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows сервер 2008, Windows server 2008 с пакетом обновления 1<br/>                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**онаусентикатионварнингдисмиссед**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





