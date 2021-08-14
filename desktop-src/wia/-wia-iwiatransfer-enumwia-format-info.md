---
description: создает перечислитель для форматов пересылки, которые поддерживает устройство Windowsного получения изображений (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Метод Ивиатрансфер:: EnumWIA_FORMAT_INFO (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669480"
---
# <a name="iwiatransferenumwia_format_info-method"></a>\_Метод сведения о формате ивиатрансфер:: енумвиа \_

создает перечислитель для форматов пересылки, которые поддерживает устройство Windowsного получения изображений (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиенум* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ \_ сведения о формате иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Адрес указателя на [**\_ \_ Информационный интерфейс формата иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) для перечислителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя интерфейса, полученного через параметр *ппиенум* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
