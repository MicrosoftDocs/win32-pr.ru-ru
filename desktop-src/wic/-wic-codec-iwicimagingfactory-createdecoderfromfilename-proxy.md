---
description: Функция-посредник для метода Креатедекодерфромфиленаме.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: Функция IWICImagingFactory_CreateDecoderFromFilename_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dabc24d17fdac881537d45e47a8cc6808a1cf805ac14025d7fdfcfa50eea8500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056634"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>IWICImagingFactory \_ креатедекодерфромфиленаме \_ -функция

Функция-посредник для метода [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **IWICImagingFactory \***

</dd> <dt>

*взфиленаме* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку, завершающуюся нулем, которая указывает имя объекта для создания или открытия.

</dd> <dt>

*пгуидвендор* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID**

Идентификатор GUID поставщика для декодера.

</dd> <dt>

*двдесиредакцесс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Доступ к объекту, который может быть доступен для чтения, записи или для того и другого.

Дополнительные сведения см. в разделе File [Security and Access \[ Rights \] Files](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*метадатаоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**Викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , используемый при создании декодера.

</dd> <dt>

*ппидекодер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

