---
title: Идевицеброкер Опендевицефроминтерфацепас, метод
description: Пытается открыть экземпляр интерфейса устройства от имени клиента. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Интерфейс API брокера доступа устройства Опендевицефроминтерфацепас
- API брокера доступа устройства Опендевицефроминтерфацепас, интерфейс Идевицеброкер
- API брокера доступа устройства интерфейса Идевицеброкер, метод Опендевицефроминтерфацепас
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412459"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>Метод Идевицеброкер:: Опендевицефроминтерфацепас

> [!Important]  
> Эти интерфейсы не поддерживаются, и их не следует использовать. Вместо этого используйте API-интерфейсы в [справочнике по программированию API для доступа к устройствам](device-access-api-c---programming-reference.md) .

Пытается открыть экземпляр интерфейса устройства от имени клиента. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*псздевицеинтерфацепас* \[ окне\]
</dt> <dd>

Открываемый экземпляр интерфейса устройства.

</dd> <dt>

*десиредакцесс* \[ окне\]
</dt> <dd>

Требуемый доступ, передаваемый в Open.

</dd> <dt>

*шаремоде* \[ окне\]
</dt> <dd>

Режим предоставления общего доступа, который должен быть передан в открытие.

</dd> <dt>

*флагсандаттрибутес* \[ окне\]
</dt> <dd>

Флаги и атрибуты, которые должны быть переданы для открытия.

</dd> <dt>

*\* фдевице* \[\]
</dt> <dd>

Результирующий обработчик, если открыт успешно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается с ошибкой, возвращается S_OK. В противном случае возвращается код ошибки HRESULT.
