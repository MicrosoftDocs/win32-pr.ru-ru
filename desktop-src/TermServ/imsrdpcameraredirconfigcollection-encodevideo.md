---
title: Свойство IMsRdpCameraRedirConfigCollection EncodeVideo
description: Указывает, является ли поток видео закодированным H. 264.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енкодевидео
- Службы удаленных рабочих столов свойства Енкодевидео, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Енкодевидео
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 9eda6fd63953425001906595b0cd8b594496e0f83974ba9d359ed43a639a4164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475964"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: Енкодевидео

Указывает, является ли поток видео закодированным H. 264.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Значение свойства

Значение, указывающее, является ли поток видео закодированным H. 264.

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