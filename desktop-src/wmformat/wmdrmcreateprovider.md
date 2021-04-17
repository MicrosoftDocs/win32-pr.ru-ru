---
title: Функция Вмдрмкреатепровидер (Вмдрмсдк. h)
description: Функция Вмдрмкреатепровидер создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Вмдрмкреатепровидер функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717821"
---
# <a name="wmdrmcreateprovider-function"></a>Функция Вмдрмкреатепровидер

Функция **вмдрмкреатепровидер** создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media. Эта функция не требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, которые не поддерживают защищенные функции DRM.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдрмпровидер* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**ивмдрмпровидер**](iwmdrmprovider.md) только что созданного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции**](drm-functions.md)
</dt> <dt>

[**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





