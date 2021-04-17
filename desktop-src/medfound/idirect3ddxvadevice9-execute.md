---
description: Выполняет операцию декодирования DirectX Video Acceleration (ДКСВА).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Метод IDirect3DDXVADevice9:: Execute (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711793"
---
# <a name="idirect3ddxvadevice9execute-method"></a>Метод IDirect3DDXVADevice9:: Execute

Выполняет операцию декодирования DirectX Video Acceleration (ДКСВА).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*функтионнум* 
</dt> <dd>

**DWORD** , содержащий один или несколько номеров функций дксва. Дополнительные сведения см. в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*пинпутдата* 
</dt> <dd>

Указатель на буфер, содержащий входные данные для операции декодирования. Значение этих данных зависит от типа поверхности и номера функции.

</dd> <dt>

*инпутсизе* 
</dt> <dd>

Размер входных данных в байтах.

</dd> <dt>

*OutputData* 
</dt> <dd>

Указатель на буфер, в который видео-ускоритель записывает выходные данные.

</dd> <dt>

*аутпутсизе* 
</dt> <dd>

Размер буфера *аутпутдата* в байтах.

</dd> <dt>

*нумбуфферс* 
</dt> <dd>

Число элементов в массиве *пбуфферинфо* .

</dd> <dt>

*пбуфферинфо* 
</dt> <dd>

Указатель на массив структур [**дксвабуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .

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

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
