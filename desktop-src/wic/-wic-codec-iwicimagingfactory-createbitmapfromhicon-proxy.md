---
description: Функция-посредник для метода Креатебитмапфромхикон.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: Функция IWICImagingFactory_CreateBitmapFromHICON_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a1e6582a7548c380d9904e9892d164a2f0778be4fe64fabaf4090b86fd932ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088326"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a>IWICImagingFactory \_ креатебитмапфромхикон \_ -функция

Функция-посредник для метода [**креатебитмапфромхикон**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*Хикон* \[ окне\]
</dt> <dd>

Тип: **Хикон**

Маркер значка для создания нового точечного рисунка из.

</dd> <dt>

*ппибитмап* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Указатель, получающий указатель на новое растровое изображение.

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



 

 




