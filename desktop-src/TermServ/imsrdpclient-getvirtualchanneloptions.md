---
title: Имсрдпклиент Жетвиртуалчаннелоптионс, метод
description: Извлекает параметры, заданные для виртуального канала.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетвиртуалчаннелоптионс
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d51ad6ccd1924c78817f76f385d65e1963b68c1b1329c3d6ba924f25a827a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059092"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>Метод Имсрдпклиент:: Жетвиртуалчаннелоптионс

Извлекает параметры, заданные для виртуального канала.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Чаннаме* \[ окне\]
</dt> <dd>

Имя виртуального канала, указанного в вызове метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*пчаноптионс* \[ заполняет\]
</dt> <dd>

Параметры, заданные для виртуального канала, заданного параметром *чаннаме* . Описание возможных вариантов см. в разделе [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

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

[**DEF по КАНАЛу \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**сетвиртуалчаннелоптионс**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





