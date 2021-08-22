---
description: Прерывать изменения состояния параметров эффектов записи.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'Метод ID3DXEffect:: Ендпараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b1d68aa1bd716ee106a5d1588a7a7060adb851185115e97d2f5f2a5d7f857c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494234"
---
# <a name="id3dxeffectendparameterblock-method"></a>Метод ID3DXEffect:: Ендпараметерблокк

Прерывать изменения состояния параметров эффектов записи.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер в блок состояния параметра.

## <a name="remarks"></a>Remarks

Все параметры эффектов, изменяющие состояние (после вызова Бегинпараметерблокк и до вызова Ендпараметерблокк), будут сохранены в блоке состояния параметра effect. Используйте Апплипараметерблокк, чтобы применить этот блок изменений состояния к системе эффектов. После завершения работы с блоком состояния используйте Делетепараметерблокк, чтобы освободить память.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Бегинпараметерблокк**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: Апплипараметерблокк**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D Елетепараметерблокк**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




