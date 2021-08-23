---
title: Сообщение WM_CAP_FILE_SAVEAS (VFW. h)
description: '\_Сообщение SAVEAS с закреплением WM \_ \_ копирует содержимое файла записи в другой файл. Это сообщение можно отправить явно или с помощью макроса Капфилесавеас.'
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- сообщение WM_CAP_FILE_SAVEAS Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687014"
---
# <a name="wm_cap_file_saveas-message"></a>\_Сообщение о \_ SAVEAS для файла ЗАкрепления WM \_

Сообщение **\_ \_ \_ SAVEAS с закреплением WM** копирует содержимое файла записи в другой файл. Это сообщение можно отправить явно или с помощью макроса [**капфилесавеас**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя целевого файла, используемого для копирования файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Remarks

Это сообщение не изменяет имя или содержимое текущего файла записи.

Если операция копирования завершается неудачно из-за ошибки переполнения диска, конечный файл автоматически удаляется.

Как правило, файл записи предварительно выделяется для самого крупного сегмента записи, и только его часть может использоваться для сбора данных. В этом сообщении копируется только часть файла, содержащего данные записи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





