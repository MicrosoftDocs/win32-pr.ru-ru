---
title: Сообщение MCIWNDM_GETLENGTH (VFW. h)
description: Сообщение МЦИВНДМ \_ DATALENGTH извлекает длину содержимого или файла, который в настоящее время используется устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетленгс.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489420"
---
# <a name="mciwndm_getlength-message"></a>Сообщение МЦИВНДМ о \_ длительности

Сообщение **МЦИВНДМ \_ DATALENGTH** извлекает длину содержимого или файла, который в настоящее время используется устройством MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетленгс**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает длину. Единицы длины зависят от текущего формата времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетленгс**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





