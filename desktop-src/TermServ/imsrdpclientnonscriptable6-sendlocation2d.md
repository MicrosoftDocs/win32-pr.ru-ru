---
title: Метод IMsRdpClientNonScriptable6 SendLocation2D
description: Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SendLocation2D
- Службы удаленных рабочих столов метода SendLocation2D, интерфейс IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, метод SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2e2e252f86249531c61922cf02f308bfaf2b76c2518ff9b420f5ec3fd80d9d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990144"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>Метод IMsRdpClientNonScriptable6:: SendLocation2D

Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Параметры

*Широта* \[ окне\]

Широта географического расположения. Допустимый диапазон значений широты — от-90,0 до 90,0 градусов.

*Долгота* \[ окне\]

Долгота географического расположения. Допустимый диапазон значений широты — от-180,0 до 180,0 градусов.

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
