---
description: Отправляется расширением диспетчера файлов для получения сведений о диске из активного окна диспетчера файлов.
title: Сообщение FM_GETDRIVEINFO (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459124"
---
# <a name="fm_getdriveinfo-message"></a>\_Сообщение FM жетдривеинфо

Отправляется расширением диспетчера файлов для получения сведений о диске из активного окна диспетчера файлов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*лпфмсгди* 
</dt> <dd>

Адрес структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , которая получает сведения о диске.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение.

## <a name="remarks"></a>Remarks

Если значение 0xFFFFFFFF возвращается в члене **двтоталспаце** или **двфриспаце** структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , то библиотека расширений должна вычислять значения или значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 




