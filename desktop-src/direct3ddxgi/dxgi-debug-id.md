---
description: Значения глобального уникального идентификатора (GUID), которые указывают производителя сообщений об отладке.
ms.assetid: 85946D30-5E49-4E4B-AC25-394ABFF0DB11
title: DXGI_DEBUG_ID (Дксгидебуг. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3642f8ece96a7a63ed6137eef14069a33a418511321a4df10cdd95e122e13397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068824"
---
# <a name="dxgi_debug_id"></a>\_идентификатор отладки \_ DXGI

Значения глобального уникального идентификатора (GUID), которые указывают производителя сообщений об отладке.



| Константа/значение                                                                                                                                                                                                                                                                                         | Описание                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_DEBUG_ALL"></span><span id="dxgi_debug_all"></span><dl> <dt>**DXGI \_ ОТЛАДКа \_ всех**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xA9, 0xcf, 0xDA, 0x8</dt> </dl>       | Все объекты Direct3D и DXGI и частные приложения.<br/>                                                                                     |
| <span id="DXGI_DEBUG_DX"></span><span id="dxgi_debug_dx"></span><dl> <dt>**DXGI \_ DEBUG \_ DX**</dt> <dt>0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7E, 0x44, 0x51, 0x28, 0x7D, 0x64</dt> </dl>         | Объекты Direct3D и DXGI.<br/>                                                                                                          |
| <span id="DXGI_DEBUG_DXGI"></span><span id="dxgi_debug_dxgi"></span><dl> <dt>**DXGI \_ ОТЛАДКа \_ DXGI**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3E, 0x98, 0x87, 0x5B, 0x5A, 0x2e, 0x2A</dt> </dl>   | DXGI.<br/>                                                                                                                               |
| <span id="DXGI_DEBUG_APP"></span><span id="dxgi_debug_app"></span><dl> <dt>**DXGI \_ ОТЛАДКа \_ приложения**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xC, 0x62</dt> </dl>         | Частные приложения. Все сообщения, добавляемые с помощью [**идксгиинфокуеуе:: аддаппликатионмессаже**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).<br/> |
| <span id="DXGI_DEBUG_D3D11"></span><span id="dxgi_debug_d3d11"></span><dl> <dt>**DXGI \_ DEBUG \_ D3D11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xBB, 0xB, 0xba, 0x82, 0x47, 0x84, 0x79, 0x8F</dt> </dl> | Direct3D 11. Определен в D3D11SDKLayers. h.<br/>                                                                                           |



## <a name="remarks"></a>Remarks

Используйте эти значения с интерфейсом [**идксгиинфокуеуе**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .

``` syntax
typedef GUID DXGI_DEBUG_ID;

DEFINE_GUID(DXGI_DEBUG_ALL, 0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8);
DEFINE_GUID(DXGI_DEBUG_DX, 0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64);
DEFINE_GUID(DXGI_DEBUG_DXGI, 0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a);
DEFINE_GUID(DXGI_DEBUG_APP, 0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62);

DEFINE_GUID(DXGI_DEBUG_D3D11, 0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f);
```

Чтобы использовать любые из этих значений GUID, включите в код Дксгидебуг. h и свяжите его с дксгуид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Дксгидебуг. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Константы DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




