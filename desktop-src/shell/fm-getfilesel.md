---
description: Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Сообщение FM_GETFILESEL (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841425"
---
# <a name="fm_getfilesel-message"></a>\_Сообщение FM жетфилесел

Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).

## <a name="parameters"></a>Параметры

<dl> <dt>

*index* 
</dt> <dd>

Отсчитываемый от нуля индекс выбранного файла для извлечения.

</dd> <dt>

*лпфмсгфс* 
</dt> <dd>

Адрес структуры [**FMS \_ жетфилесел**](fms-getfilesel.md) , которая получает сведения о выделенном фрагменте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс выбранного файла, который был получен.

## <a name="remarks"></a>Remarks

Расширение может использовать сообщение [**FM \_ жетселкаунт**](fm-getselcount.md) для получения числа выбранных файлов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> <dt>

[**FM \_ жетфилеселлфн**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ жетселкаунтлфн**](fm-getselcountlfn.md)
</dt> </dl>

 

 




