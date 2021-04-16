---
title: Метод IMsRdpCameraRedirConfigCollection AddConfig
description: Добавляет объект Имсрдпкамераредирконфиг в коллекцию (соответствующая камера не должна быть подключена).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддконфиг
- Службы удаленных рабочих столов метода Аддконфиг, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, метод Аддконфиг
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536380"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>Метод Имсрдпкамераредирконфигколлектион:: Аддконфиг

Добавляет объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекцию (соответствующая камера не должна быть подключена).

## <a name="syntax"></a>Синтаксис

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Параметры

*symbolicLink* \[ окне\]

Символьная ссылка для нового объекта [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) .

*фредиректед* \[ окне\]

Указывает, будет ли перенаправлена новая камера по умолчанию.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>