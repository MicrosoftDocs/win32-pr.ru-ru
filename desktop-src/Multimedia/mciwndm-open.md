---
title: Сообщение MCIWNDM_OPEN (VFW. h)
description: МЦИВНДМ \_ Open Message открывает устройство MCI и связывает его с окном мЦивнд.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- сообщение MCIWNDM_OPEN Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bebf9573303e3560b385425e7642106120c41456a21c1c4b80bc158328a864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428904"
---
# <a name="mciwndm_open-message"></a>МЦИВНДМ \_ открытое сообщение

**МЦивндм \_ Open** Message открывает устройство MCI и связывает его с окном мЦивнд. Для устройств MCI, использующих файлы данных, этот макрос также может открыть указанный файл данных, присвоить имя новому создаваемому файлу или открыть диалоговое окно, позволяющее пользователю выбрать открываемый файл. Это сообщение можно отправить явно или с помощью макроса [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*вфлагс*
</dt> <dd>

Флаги, связанные с открываемым устройством или файлом. \_Флаг New мЦивндопенф указывает, что новый файл создается с именем, указанным в **сзфиле**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*сзфиле*
</dt> <dd>

Указатель на строку, завершающуюся нулем, указывающую имя файла или устройства MCI, которое нужно открыть. Укажите значение 1 для этого параметра, чтобы отобразить диалоговое окно Открыть.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





