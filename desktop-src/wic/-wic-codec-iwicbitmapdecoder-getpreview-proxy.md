---
description: Функция-посредник для метода OnPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: Функция IWICBitmapDecoder_GetPreview_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692227"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a>\_ \_ Функция прокси Ивикбитмапдекодер-Preview

Функция-посредник для метода [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Указатель на этот объект [_ *ивикбитмапдекодер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*ппибитмапсаурце* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Указатель, получающий указатель на битовую карту предварительного просмотра, если поддерживается.

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



 

 




