---
description: Создает объект преобразования цвета, реализующий Ивикколортрансформ. Этот COM-объект поддерживает объектную модель свободной потоковой модели.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Функция WICCreateColorTransform_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704173"
---
# <a name="wiccreatecolortransform_proxy-function"></a>Виккреатеколортрансформ \_ -функция прокси

Создает объект преобразования цвета, реализующий [**ивикколортрансформ**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Этот COM-объект поддерживает объектную модель свободной потоковой модели.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиколортрансформ* \[ заполняет\]
</dt> <dd>

Созданное преобразование цвета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
