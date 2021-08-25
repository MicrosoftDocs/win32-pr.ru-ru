---
title: Идевицеакцессполицичекк Девицеинтерфацеклассакцессчекквискаллингсреад, метод
description: Этот API определит, имеет ли маркер текущего контекста доступ к указанному классу интерфейса устройства. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Интерфейс API брокера доступа устройства Девицеинтерфацеклассакцессчекквискаллингсреад
- API брокера доступа устройства Девицеинтерфацеклассакцессчекквискаллингсреад, интерфейс Идевицеакцессполицичекк
- API брокера доступа устройства интерфейса Идевицеакцессполицичекк, метод Девицеинтерфацеклассакцессчекквискаллингсреад
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635354"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>Идевицеакцессполицичекк: метод:D Евицеинтерфацеклассакцессчекквискаллингсреад

> [!Important]  
> Эти интерфейсы не поддерживаются, и их не следует использовать. Вместо этого используйте API-интерфейсы в [справочнике по программированию API для доступа к устройствам](device-access-api-c---programming-reference.md) .

Этот API определит, имеет ли маркер текущего контекста доступ к указанному классу интерфейса устройства. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*псздевицеинтерфацеклассгуид* \[ окне\]
</dt> <dd>

Идентификатор GUID класса интерфейса устройства, для которого необходимо проверить доступ.

</dd> <dt>

*двклиентсреадид* \[ окне\]
</dt> <dd>

Идентификатор клиентского потока, в котором при необходимости должен отображаться любой связанный пользовательский интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается с ошибкой, возвращается S_OK. В противном случае будет возвращен код ошибки HRESULT.
