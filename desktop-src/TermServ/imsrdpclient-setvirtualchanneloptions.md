---
title: Имсрдпклиент Сетвиртуалчаннелоптионс, метод
description: задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Сетвиртуалчаннелоптионс
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871588"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>Метод Имсрдпклиент:: Сетвиртуалчаннелоптионс

задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.

вызовите этот метод после вызова метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) , но перед установкой соединения с помощью метода [**Подключение**](imstscax-connect.md) . Этот метод задает дополнительные параметры для виртуальных каналов, созданных с помощью **креатевиртуалчаннелс**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Чаннаме* \[ окне\]
</dt> <dd>

Имя виртуального канала, указанного в вызове метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*чаноптионс* \[ окне\]
</dt> <dd>

Параметры, устанавливаемые для виртуального канала, заданного параметром *чаннаме* . Описание возможных вариантов см. в разделе [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Дополнительные сведения см. в разделе "Примечания".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

В качестве примера использования этого метода можно объявить канал как удаленное управление, задав **\_ \_ Постоянный флаг удаленного \_ управления \_ для параметра канала** . Это означает, что канал не будет закрыт, когда удаленный элемент управления подключается к сеансу, подключенному к клиенту, или отключается от него. Дополнительные сведения см. в разделе [постоянные виртуальные каналы удаленного управления](remote-control-persistent-virtual-channels.md).

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>См. также

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

[**DEF по КАНАЛу \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**жетвиртуалчаннелоптионс**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





