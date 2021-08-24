---
description: Создает устройство декодера DirectX Video Acceleration (ДКСВА).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Метод IDirect3DVideoDevice9:: Креатедксвадевице (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555734"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>Метод IDirect3DVideoDevice9:: Креатедксвадевице

Создает устройство декодера DirectX Video Acceleration (ДКСВА).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Указатель на идентификатор GUID, указывающий создаваемое устройство.

</dd> <dt>

*пункомпдата* 
</dt> <dd>

Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , которая задает формат несжатого изображения.

</dd> <dt>

*pData* 
</dt> <dd>

Указатель на структуру **\_ коннектмоде дксва** , которая указывает режим дксва и ограниченный профиль.

</dd> <dt>

*DataSize* 
</dt> <dd>

Размер структуры **\_ коннектмоде дксва** в байтах.

</dd> <dt>

*ппдксвадевице* 
</dt> <dd>

Получает указатель на интерфейс [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) . Вызывающий объект должен освободить интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




