---
description: Функция-посредник для метода Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: Функция IWICBitmapFlipRotator_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701441"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a>Ивикбитмапфлипротатор \_ инициализировать \_ прокси-функцию

Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _

Указатель на этот объект [_ *ивикбитмапфлипротатор* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

</dd> <dt>

*писаурце* \[ окне\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Источник входного точечного рисунка.

</dd> <dt>

_options * \[ в\]
</dt> <dd>

Тип: **[ **викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**

[**Викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) для отражения или поворота изображения.

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



 

 




