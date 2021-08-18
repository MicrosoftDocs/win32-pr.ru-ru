---
description: регистрирует выполняющееся приложение для уведомления о событии Windowsного получения изображений (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккинтерфаце (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965644"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Метод IWiaDevMgr2:: Регистеревенткаллбаккинтерфаце

регистрирует выполняющееся приложение для уведомления о событии Windowsного получения изображений (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает уникальный идентификатор устройства WIA 2,0. Присвойте этому параметру **значение NULL** , чтобы зарегистрировать событие на всех устройствах WIA 2,0.

</dd> <dt>

*певентгуид* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID**

Указывает указатель на идентификатор события, для которого регистрируется приложение. См. раздел [идентификаторы событий WIA](-wia-wia-event-identifiers.md) для стандартных идентификаторов событий.

</dd> <dt>

*пивиаевенткаллбакк* \[ окне\]
</dt> <dd>

Тип: **[ **ивиаевенткаллбакк**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Указывает указатель на интерфейс [**ивиаевенткаллбакк**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) , который WIA 2,0 использует для отправки уведомления о событии.

</dd> <dt>

*певентобжект* \[ заполняет\]
</dt> <dd>

Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Получает адрес указателя на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает стандартные коды ошибок COM или следующие.



| Код возврата                                                                               | Описание                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ нотимпл**</dt> </dl> | Интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) не может быть возвращен. <br/> |



 

## <a name="remarks"></a>Remarks

> [!WARNING]
> Использование методов [**ивиадевмгр:: регистеревенткаллбаккинтерфаце**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: регистеревенткаллбаккинтерфаце** и [**девицеманажер. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) из того же процесса после перезапуска службы изображений может привести к нарушению прав доступа, если функции использовались до остановки службы.

 

Когда приложения WIA 2,0 начинают выполняться, они используют этот метод для регистрации для получения событий устройства. Это предотвращает перезапуск приложения при возникновении другого события, для которого оно зарегистрировано. После того как приложение вызывает **IWiaDevMgr2:: регистеревенткаллбаккинтерфаце** , чтобы зарегистрироваться для получения событий WIA 2,0 с устройства, зарегистрированные события направляются в программу WIA 2,0.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *певентобжект* .

> [!Note]  
> В многопоточном приложении обратный вызов уведомления о событии может находиться в другом потоке из того, который зарегистрировал обратный вызов.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
