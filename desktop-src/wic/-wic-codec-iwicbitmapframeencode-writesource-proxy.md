---
description: Функция-посредник для метода Вритесаурце.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: Функция IWICBitmapFrameEncode_WriteSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272967"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a>Ивикбитмапфраминкоде \_ вритесаурце \_ -функция

Функция-посредник для метода [**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _

Указатель на этот объект [_ *ивикбитмапфраминкоде* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

</dd> <dt>

*пибитмапсаурце* \[ окне\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Источник точечного рисунка для кодирования.

</dd> <dt>

_prc * \[ в\]
</dt> <dd>

Тип: **[**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Прямоугольник размера источника точечного рисунка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




