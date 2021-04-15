---
title: Имстскаксевентс Онрецеиведтспубликкэй, метод
description: Вызывается во время последовательности подключения, когда клиент получает открытый ключ с сервера. Это событие вызывается, только если свойство Нотифитспубликкэй имеет значение VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онрецеиведтспубликкэй
- Службы удаленных рабочих столов метода Онрецеиведтспубликкэй, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онрецеиведтспубликкэй
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491325"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>Метод Имстскаксевентс:: Онрецеиведтспубликкэй

Вызывается во время последовательности подключения, когда клиент получает открытый ключ с сервера. Это событие вызывается, только если свойство **нотифитспубликкэй** имеет значение **Variant \_ true**. Это происходит после [**подключения**](imstscaxevents-onconnecting.md), но перед [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) и [**подключением**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Синтаксис


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PublicKey* \[ окне\]
</dt> <dd>

Содержит открытый ключ удаленного компьютера.

</dd> <dt>

*пфконтинуелогон* \[ заполняет\]
</dt> <dd>

Указатель на переменную **\_ bool типа Variant** , которая получает, должен ли продолжаться процесс входа в систему.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

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

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





