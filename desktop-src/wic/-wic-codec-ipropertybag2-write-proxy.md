---
description: 'Функция прокси компонента Windows Imaging Component (WIC) для IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: Функция IPropertyBag2_Write_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343252"
---
# <a name="ipropertybag2_write_proxy-function"></a>IPropertyBag2 \_ \_ -функция записи

Функция прокси компонента Windows Imaging Component (WIC) для IPropertyBag2:: Write.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _

парамдеск

</dd> <dt>

_cProperties * \[ в\]
</dt> <dd>

Тип: **ulong**

</dd> <dt>

*ппропбаг* \[ окне\]
</dt> <dd>

Тип: **[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _

</dd> <dt>

_pvarValue * \[ в\]
</dt> <dd>

Тип: **Variant \** _

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



 

