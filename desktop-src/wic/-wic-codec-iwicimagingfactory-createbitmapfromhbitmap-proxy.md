---
description: Функция-посредник для метода Креатебитмапфромхбитмап.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: Функция IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684204"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a>IWICImagingFactory \_ креатебитмапфромхбитмап \_ -функция

Функция-посредник для метода [**креатебитмапфромхбитмап**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hBitmap * \[ в\]
</dt> <dd>

Тип: **хбитмап**

Маркер точечного рисунка для создания точечного рисунка из.

</dd> <dt>

*хпалетте* \[ окне\]
</dt> <dd>

Тип: **хпалетте**

Маркер палитры, используемый для создания точечного рисунка.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **викбитмапалфачаннелоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**

Параметры альфа-канала для создания точечного рисунка.

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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




