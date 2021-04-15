---
description: Создает перечислитель для форматов обмена, которые поддерживает устройство Windows Image (WIA) 2,0.
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
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682736"
---
# <a name="iwiatransferenumwia_format_info-method"></a>\_Метод сведения о формате ивиатрансфер:: енумвиа \_

Создает перечислитель для форматов обмена, которые поддерживает устройство Windows Image (WIA) 2,0.

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

## <a name="remarks"></a>Комментарии

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя интерфейса, полученного через параметр *ппиенум* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
