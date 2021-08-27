---
description: Функция-посредник для метода Креатекуеривритерфромреадер.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: Функция IWICImagingFactory_CreateQueryWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6e03da055b5e48e21c044ce1708a8a8871c30fabeb860e486cde398650c23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711462"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a>IWICImagingFactory \_ креатекуеривритерфромреадер \_ -функция

Функция-посредник для метода [**креатекуеривритерфромреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*пикуериреадер* \[ окне\]
</dt> <dd>

Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Средство чтения запросов метаданных, из которого создается модуль записи метаданных.

</dd> <dt>

*пгуидвендор* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID**

Идентификатор GUID поставщика для модуля записи запросов метаданных.

</dd> <dt>

*ппикуеривритер* \[ заполняет\]
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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), Windows \[ только классические приложения Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




