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
ms.openlocfilehash: dd15dfdbd35db56262487482e811210970852dcee4e791d710e0551b84e9e620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777214"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




