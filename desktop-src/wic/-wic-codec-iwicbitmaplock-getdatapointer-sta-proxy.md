---
description: Функция-посредник для метода Жетдатапоинтер.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Функция IWICBitmapLock_GetDataPointer_STA_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b693c78ba3a3d7c68c33f68ec1494997536ffb10272cc384d89d9e94ded7145b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206751"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>Ивикбитмаплокк \_ жетдатапоинтер \_ STA \_ -функция

Функция-посредник для метода [**жетдатапоинтер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Указатель на этот объект [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

</dd> <dt>

*пкббуфферсизе* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий размер буфера.

</dd> <dt>

*ппбдата* \[ заполняет\]
</dt> <dd>

Тип: **Byte \* \***

Указатель, получающий указатель на верхний левый пиксель в заблокированном прямоугольнике.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), Windows \[ только классические приложения Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




