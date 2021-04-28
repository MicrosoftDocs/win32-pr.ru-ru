---
description: IWICMetadataQueryReader_GetContainerFormat_Proxy функция-прокси для метода Жетконтаинерформат.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Функция IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097142"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a>Ивикметадатакуериреадер \_ жетконтаинерформат \_ -функция

Функция-посредник для метода [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Указатель на этот объект [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*пгуидконтаинерформат* \[ заполняет\]
</dt> <dd>

Тип: **GUID \***

Указатель, который получает идентификатор GUID формата коинтаинер.

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



 

 




