---
description: Функция-посредник для метода GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: Функция IWICMetadataQueryReader_GetEnumerator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674227"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a>\_ \_ Функция-посредник ивикметадатакуериреадер GetEnumerator

Функция-посредник для метода [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Указатель на этот объект [_ *ивикметадатакуериреадер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*ппиенумстринг* \[ заполняет\]
</dt> <dd>

Тип: **иенумстринг \* \***

Указатель, получающий указатель на перечислитель метаданных.

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



 

 




