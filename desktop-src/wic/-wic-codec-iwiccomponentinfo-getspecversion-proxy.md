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
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713121"
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

Тип: **[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Указатель на этот объект [_ *ивиккомпонентинфо* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*кчспекверсион* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взспекверсион* .

</dd> <dt>

*взспекверсион* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \** _

При возврате из этого метода содержит язык и региональные параметры, инвариент строку версии спецификации компонента. Формат версии — NN. NN. NN. NN.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий фактическую длину версии спецификации компонента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




