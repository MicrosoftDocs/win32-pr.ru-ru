---
description: Инициализирует Ивикколортрансформ с IWICBitmapSource и преобразует его из одного Ивикколорконтекст в другой.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Функция IWICColorTransform_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704368"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Ивикколортрансформ \_ инициализировать \_ прокси-функцию

Инициализирует [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) с [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) и преобразует его из одного [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) в другой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиколортрансформ* \[ окне\]
</dt> <dd>

Тип: **[ **ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Преобразование цвета для инициализации.

</dd> <dt>

*пибитмапсаурце* \[ окне\]
</dt> <dd>

Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Источник растрового изображения, используемый для инициализации преобразования цвета.

</dd> <dt>

*пиконтекстсаурце* \[ окне\]
</dt> <dd>

Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Источник цветового контекста.

</dd> <dt>

*пиконтекстдест* \[ окне\]
</dt> <dd>

Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Назначение контекста цвета.

</dd> <dt>

*пикселфмтдест* \[ окне\]
</dt> <dd>

Тип: **рефвикпикселформатгуид**

Идентификатор GUID требуемого формата пикселей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




