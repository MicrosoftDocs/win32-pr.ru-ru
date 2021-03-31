---
description: Функция-посредник для метода Креатекуеривритер.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: Функция IWICImagingFactory_CreateQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817105"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a>IWICImagingFactory \_ креатекуеривритер \_ -функция

Функция-посредник для метода [**креатекуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_guidMetadataFormat * \[ в\]
</dt> <dd>

Тип: **рефгуид**

Идентификатор GUID для требуемого формата метаданных.

</dd> <dt>

*пгуидвендор* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID* _

Идентификатор GUID поставщика модуля записи метаданных.

</dd> <dt>

_ppIQueryWriter * \[ out\]
</dt> <dd>

Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Указатель, получающий указатель на новый [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).

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



 

 




