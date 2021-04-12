---
description: Завершает обработку для создания декодированного изображения.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Метод IDirect3DDXVADevice9:: Ендфраме (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155190"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>Метод IDirect3DDXVADevice9:: Ендфраме

Завершает обработку для создания декодированного изображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сиземискдата* 
</dt> <dd>

Размер буфера, заданного параметром *пмискдата*, в байтах. Значение должно быть равно 2.

</dd> <dt>

*пмискдата* 
</dt> <dd>

Указатель на буфер, содержащий данные для ускорителя видео. Этот буфер должен содержать тот же индекс кадра, который был передан методу [**IDirect3DDXVADevice9:: бегинфраме**](idirect3ddxvadevice9-beginframe.md) в параметре *пинпутдата* .

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

 

 




