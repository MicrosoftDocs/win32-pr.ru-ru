---
description: Задает адрес конечной точки, используемый для подключения к удаленному модулю.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиртопиренгине:: Сетплайбаккендпоинт'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 81f3743c9f1cca5a763df23087d7703b79d198a9cd780f9a398017c53afaabfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721801"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Метод Ипиртопиренгине:: Сетплайбаккендпоинт

Задает адрес конечной точки, используемый для подключения к удаленному модулю.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a>Параметры

*бусеаусентикатион*   
значение true, чтобы использовать проверку подлинности; в противном случае — значение false.

*конечной*   
Строка COM, содержащая адрес конечной точки.

*сессионкэй*   
Строка COM, содержащая ключ сеанса, используемый для шифрования.

*ремотеверсион*   
Указывает версию используемого удаленного обработчика.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипиртопиренгине**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
