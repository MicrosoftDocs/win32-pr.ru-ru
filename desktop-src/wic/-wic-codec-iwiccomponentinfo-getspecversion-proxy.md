---
description: Функция-посредник для метода Жетспекверсион.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: Функция IWICComponentInfo_GetSpecVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a29b57e84b7cf9ceee67ac4f64ac090e697366fbe0698a891c8fbcc87e3ff5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206587"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>Ивиккомпонентинфо \_ жетспекверсион \_ -функция

Функция-посредник для метода [**жетспекверсион**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
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

*кчспекверсион* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взспекверсион* .

</dd> <dt>

*взспекверсион* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \***

При возврате из этого метода содержит язык и региональные параметры, инвариент строку версии спецификации компонента. Формат версии — NN. NN. NN. NN.

</dd> <dt>

*пкчактуал* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий фактическую длину версии спецификации компонента.

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



 

 




