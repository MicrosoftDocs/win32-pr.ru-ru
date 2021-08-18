---
title: Имстскакс Креатевиртуалчаннелс, метод
description: Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Креатевиртуалчаннелс
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ef4e7c8471c655d4ecfaf54a1c4b0f35b2362c67c334bd94e57da8e99d390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138487"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>Метод Имстскакс:: Креатевиртуалчаннелс

Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Список допустимых имен виртуальных каналов с разделителями-запятыми. Длина каждого имени в списке может быть не меньше одного, а не более семи алфавитных символов. Длина всей строки может быть как минимум одной длиной не более 300 алфавитных символов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . Возвращает значение **E \_ INVALIDARG** , если переданный параметр не соответствует заданным критериям.

## <a name="remarks"></a>Remarks

вызовите этот метод перед вызовом метода [**Подключение**](imstscax-connect.md) .

Сведения об ограничениях именования виртуальных каналов см. в статье [Регистрация клиента виртуального канала](virtual-channel-client-registration.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





