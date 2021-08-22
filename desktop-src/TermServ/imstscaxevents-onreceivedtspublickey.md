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
ms.openlocfilehash: 73f2b12b59cbe8e6b7c5f8e614e2aed047d4f467117fa211839521fedc7f333b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009484"
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

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows сервер 2008, Windows server 2008 с пакетом обновления 1<br/>                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





