---
description: Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Метод IDirect3DVideoDevice9:: Жетдксваинтерналинфо (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711345"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>Метод IDirect3DVideoDevice9:: Жетдксваинтерналинфо

Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Указатель на идентификатор GUID, указывающий профиль ДКСВА. Чтобы получить список поддерживаемых профилей, вызовите [**IDirect3DVideoDevice9:: жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*пункомпдата* 
</dt> <dd>

Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , указывающую размер и формат пикселей для несжатых данных.

</dd> <dt>

*пмеморюсед* 
</dt> <dd>

Получает объем вспомогательной памяти, выделяемой HAL, в байтах.

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

 

 




