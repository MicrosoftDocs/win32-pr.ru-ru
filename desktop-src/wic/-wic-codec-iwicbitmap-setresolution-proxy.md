---
description: IWICBitmap_SetResolution_Proxy функция-прокси для метода Сетресолутион.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: Функция IWICBitmap_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a32fa4e0d830d5307bc2927a1d5b6cb0a40e5b21f86517dc4421a0ce246a2ab8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056704"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a>Ивикбитмап \_ сетресолутион \_ -функция

Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Указатель на этот объект [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*дпикс* \[ окне\]
</dt> <dd>

Тип: **Double**

Разрешение по горизонтали.

</dd> <dt>

*дпий* \[ окне\]
</dt> <dd>

Тип: **Double**

Разрешение по вертикали.

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



 

 




