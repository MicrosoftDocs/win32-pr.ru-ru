---
title: Имстскаксевентс Ончаннелрецеиведдата, метод
description: Вызывается, когда клиент получает данные в виртуальном канале, поддерживающем скрипт.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ончаннелрецеиведдата
- Службы удаленных рабочих столов метода Ончаннелрецеиведдата, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Ончаннелрецеиведдата
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135758"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Метод Имстскаксевентс:: Ончаннелрецеиведдата

Вызывается, когда клиент получает данные в виртуальном канале, поддерживающем скрипт.

## <a name="syntax"></a>Синтаксис


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*чаннаме* \[ окне\]
</dt> <dd>

Имя виртуального канала, на котором были получены данные. Это имя соответствует одному из каналов, созданных при вызове метода [**имстскакс:: креатевиртуалчаннелс**](imstscax-createvirtualchannels.md).

</dd> <dt>

*данные* \[ окне\]
</dt> <dd>

Данные, полученные в виртуальном канале с помощью скрипта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Дополнительные сведения об этом событии см. в статье [реализация виртуальных каналов с использованием скриптов с помощью веб-подключение к удаленному рабочему столу](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





