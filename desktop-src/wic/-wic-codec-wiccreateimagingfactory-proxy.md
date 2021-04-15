---
description: Функция-посредник для создания IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Функция WICCreateImagingFactory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702390"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>Виккреатеимагингфактори \_ -функция прокси

Функция-посредник для создания [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Сдкверсион* \[ окне\]
</dt> <dd>

Тип: **uint**

</dd> <dt>

*ппиимагингфактори* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция является вспомогательной функцией для создания фабрики WIC для явной компоновки DLL, которая была необходима для Windows XP. В нормальном использовании вместо этого следует использовать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (см. [фабрики классов API WIC](./-wic-api.md#class-factories)), так как они всегда включаются во все более новые версии Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>виндовскодекс. lib</dt> </dl> |



 

