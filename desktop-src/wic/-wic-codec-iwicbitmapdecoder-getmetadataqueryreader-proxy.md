---
description: Функция-посредник для метода Жетметадатакуериреадер.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: Функция IWICBitmapDecoder_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343222"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a>Ивикбитмапдекодер \_ жетметадатакуериреадер \_ -функция

Функция-посредник для метода [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Указатель на этот объект [_ *ивикбитмапдекодер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*ппиметадатакуериреадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***

Указатель, получающий указатель на метаданные.

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



 

 




