---
title: Свойство IMsRdpCameraRedirConfigCollection ByIndex
description: Возвращает объект Имсрдпкамераредирконфиг по его индексу в коллекции.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Биндекс
- Службы удаленных рабочих столов свойства Биндекс, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Биндекс
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 375c0b110975c6ca791bbbe1f61a5b597b00316242484cd68ef018b7ef4ea88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138967"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: Биндекс

Возвращает объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) по его индексу в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Значение свойства

Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий указанному индексу.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>