---
title: Имсрдпклиент RequestClose, метод
description: запрашивает корректное завершение работы элемента управления удаленный рабочий стол ActiveX.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae812c27b0c280ca3a6cd879d5af86181de85793ec6092441fb83b45c74d8656
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010185"
---
# <a name="imsrdpclientrequestclose-method"></a>Метод Имсрдпклиент:: RequestClose

запрашивает корректное завершение работы элемента управления удаленный рабочий стол ActiveX. Корректное завершение работы может включать в себя завершение сеанса службы удаленных рабочих столов пользователя, но не завершает работу сервера узла сеансов удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклосестатус* \[ заполняет\]
</dt> <dd>

Значение из перечисления [**контролклосестатус**](controlclosestatus.md) , указывающее, может ли приложение немедленно закрыть элемент управления. Ниже приведен список возможных значений.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**контролклосеканпроцеед** (символ 0x0000)


</dt> <dd>

Приложение контейнера может перейти к немедленному закрытию элемента управления. Это значение может также означать, что соединение уже завершено.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**контролклосеваитфоревентс** (0x0001)


</dt> <dd>

Приложение контейнера не должно немедленно закрыть элемент управления; приложение должно ожидать одно из событий, описанных в следующем разделе "Примечания", перед закрытием.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Если параметр *пклосестатус* равен **контролклосеваитфоревентс**, то приложение должно подождать одно из следующих событий, прежде чем приложение закроет элемент управления:

-   [**Имстскаксевентс:: Ondisconnectо**](imstscaxevents-ondisconnected.md). Если пользователь не вошел в сеанс службы удаленных рабочих столов, приложение может вызвать функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) , чтобы уничтожить все окна и закрыть элемент управления.
-   [**Имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md). Если пользователь вошел в сеанс службы удаленных рабочих столов, элемент управления запускает событие **онконфирмклосе** . Это событие позволяет приложению запрашивать пользователя о том, следует ли закрыть подключение. Если пользователь ответит на запрос, приложение контейнера может вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) для уничтожения всех окон и закрыть элемент управления.

**RequestClose** позволяет приложению-контейнеру запрашивать пользователя о необходимости закрыть подключение. Дополнительные сведения см. в разделе [**имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md).

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**Имстскаксевентс:: Онконфирмклосе**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**Имстскаксевентс:: ondisconnectо**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

