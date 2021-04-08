---
description: Функция-посредник для метода Креатеметадатавритерфромреадер.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: Функция IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910420"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a>Ивиккомпонентфактори \_ креатеметадатавритерфромреадер \_ -функция

Функция-посредник для метода [**креатеметадатавритерфромреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _

Указатель на этот объект [_ *ивиккомпонентфактори* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .

</dd> <dt>

*пиреадер* \[ окне\]
</dt> <dd>

Тип: **[**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _

</dd> <dt>

_pguidVendor * \[ в\]
</dt> <dd>

Тип: **константа \* GUID* _

</dd> <dt>

_ppIWriter * \[ out\]
</dt> <dd>

Тип: **[ **ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***

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



 

 




