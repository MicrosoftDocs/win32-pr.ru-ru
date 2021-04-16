---
title: Свойство IMsRdpCameraRedirConfigCollection EncodingQuality
description: Задает качество кодирования (скорость потока).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енкодингкуалити
- Службы удаленных рабочих столов свойства Енкодингкуалити, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Енкодингкуалити
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494157"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: Енкодингкуалити

Задает качество кодирования (скорость потока).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Значение свойства

Одно из следующих значений перечисления **камераредиренкодингкуалити** , определяющее качество кодирования (скорость потока).

| Имя элемента перечисления | Значение |
|-----------------|--------|
| енкодингкуалитилов | 0x0000 |
| енкодингкуалитимедиум | 0x0001 |
| енкодингкуалитихигх | 0x0002 |

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