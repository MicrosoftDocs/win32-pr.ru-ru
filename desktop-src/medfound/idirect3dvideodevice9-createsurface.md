---
description: Создает сжатую поверхность для декодирования DirectX Video Acceleration (ДКСВА).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'Метод IDirect3DVideoDevice9:: Креатесурфаце (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156174"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>Метод IDirect3DVideoDevice9:: Креатесурфаце

Создает сжатую поверхность для декодирования DirectX Video Acceleration (ДКСВА).

Чтобы получить требования к поверхности, вызовите метод [**IDirect3DVideoDevice9:: жетдксвакомпресседбуфферинфо**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) и изучите возвращенные структуры [**дксвакомпбуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Width* 
</dt> <dd>

Ширина поверхности в пикселях. Установите этот параметр равным **дксвакомпбуфферинфо. видстокреате**.

</dd> <dt>

*Height* 
</dt> <dd>

Высота поверхности в пикселях. Установите этот параметр равным **дксвакомпбуфферинфо. хеигхттокреате**.

</dd> <dt>

*Буферы обмена* 
</dt> <dd>

Число задних буферов. Этот параметр может быть равен нулю.

</dd> <dt>

*Формат* 
</dt> <dd>

Формат пикселей, указанный как значение **D3DFORMAT** . Установите этот параметр равным **дксвакомпбуфферинфо. Format**.

</dd> <dt>

*Пул.* 
</dt> <dd>

Пул памяти, в котором создается поверхность, указанная в качестве значения **D3DPOOL** . Установите этот параметр равным **дксвакомпбуфферинфо. pool**.

</dd> <dt>

*Использование* 
</dt> <dd>

Побитовая операция **или** для одной или нескольких констант **D3DUSAGE** . Установите этот параметр равным **дксвакомпбуфферинфо. Usage**.

</dd> <dt>

*ппсурфаце* 
</dt> <dd>

Получает указатель на интерфейс **IDirect3DSurface9** . Вызывающий объект должен освободить интерфейс.

</dd> <dt>

*пшаредхандле* 
</dt> <dd>

Зарезервировано. Задайте **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




