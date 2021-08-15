---
description: Функция-посредник для метода WebMethod.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: Функция IWICComponentInfo_GetAuthor_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c83d42f499c8f821f5b342f08749a2167aac9cc61334fe2fc2d9e9134b5e2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206675"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>\_ \_ Функция прокси Ивиккомпонентинфо-Author

Функция-посредник для [**метода WebMethod**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Указатель на этот объект [**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*кчаусор* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взаусор* .

</dd> <dt>

*взаусор* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \***

Указатель, получающий имя автора компонента.

Возвращаемая строка зависит от языкового стандарта, 1033 по умолчанию.

</dd> <dt>

*пкчактуал* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий фактическую длину имени авторов компонента.

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



 

 




