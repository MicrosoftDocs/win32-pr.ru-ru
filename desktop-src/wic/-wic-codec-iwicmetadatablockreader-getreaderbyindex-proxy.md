---
description: Функция-посредник для метода Жетреадербиндекс.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: Функция IWICMetadataBlockReader_GetReaderByIndex_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1540e6ff0e24125f9381c0dd177dd9dc77ea6fb7f9096d45b88fd7489704f496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965193"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a>Ивикметадатаблоккреадер \_ жетреадербиндекс \_ -функция

Функция-посредник для метода [**жетреадербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\***

Указатель на этот объект [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

</dd> <dt>

*ниндекс* \[ окне\]
</dt> <dd>

Тип: **uint**

</dd> <dt>

*ппиметадатареадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***

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



 

 




