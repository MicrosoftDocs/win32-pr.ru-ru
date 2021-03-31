---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Представляет пару координат x и y в двухмерном пространстве. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273504"
---
# <a name="d2d1_point_2u"></a>D2D1 \_ точка \_ 2U

Представляет пару координат x и y в двухмерном пространстве.


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a>Комментарии

Точки в Direct2D представлены структурами [**D2D1 Point \_ \_ 2F**](d2d1-point-2f.md) или **D2D1 \_ Point \_ 2U** . Оба содержат пару координат x и y в двухмерном пространстве. Структура **D2D1 \_ точки \_ 2F** сохраняет координаты как значения **float** , а структура **\_ \_ типоразмера 2U в D2D1 Point** сохраняет их как значения **UINT32** .

**D2D1 \_ ТОЧКА \_ 2U** — это новое имя уже определенного типа для [**точки D2D с типом \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (включение D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Точка D2D с \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[**\_Точка D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





