---
description: Функция-посредник для метода Сетметадатабинаме.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: Функция IWICMetadataQueryWriter_SetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5ec3d018856b087762de70d6e2aea3e1f473db96b7ad989a62b3dfc2b5d3e691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206389"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a>Ивикметадатакуеривритер \_ сетметадатабинаме \_ -функция

Функция-посредник для метода [**сетметадатабинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\***

Указатель на этот объект [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .

</dd> <dt>

*взнаме* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Имя элемента метаданных.

</dd> <dt>

*сервер* \[ окне\]
</dt> <dd>

Тип: **const [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \***

Заданные метаданные.

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



 

