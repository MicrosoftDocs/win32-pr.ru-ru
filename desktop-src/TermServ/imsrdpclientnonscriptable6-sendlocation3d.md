---
title: Метод IMsRdpClientNonScriptable6 SendLocation3D
description: Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SendLocation3D
- Службы удаленных рабочих столов метода SendLocation3D, интерфейс IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, метод SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494145"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>Метод IMsRdpClientNonScriptable6:: SendLocation3D

Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>Параметры

*Широта* \[ окне\]

Широта географического расположения. Допустимый диапазон значений широты — от-90,0 до 90,0 градусов.

*Долгота* \[ окне\]

Долгота географического расположения. Допустимый диапазон значений широты — от-180,0 до 180,0 градусов.

*Высота высотой* \[ окне\]

Высота географического расположения в метрах.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1709 (сборка 16299)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 определен как 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
