---
title: Свойство IMsRdpCameraRedirConfigCollection RedirectByDefault
description: Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректбидефаулт
- Службы удаленных рабочих столов свойства Редиректбидефаулт, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Редиректбидефаулт
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8c95431132acf5e3c08ede859520c844c4cae542f6b07dcb8e5781726078e754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475874"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: Редиректбидефаулт

Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a>Значение свойства

Значение, указывающее, перенаправляется ли новая камера по умолчанию.

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