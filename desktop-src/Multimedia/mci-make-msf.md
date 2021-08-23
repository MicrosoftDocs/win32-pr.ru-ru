---
title: Макрос MCI_MAKE_MSF (МЦиапи. h)
description: С помощью \_ MCI \_ макрос MSF создает значение времени в формате упакованных минут/секунд/кадров (MSF) с учетом заданных минут, секунд и значений кадров.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF макрос Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690134"
---
# <a name="mci_make_msf-macro"></a>MCI \_ делает \_ макрос MSF

С помощью **MCI макрос \_ \_ MSF** создает значение времени в формате упакованных минут/секунд/кадров (MSF) с учетом заданных минут, секунд и значений кадров.

## <a name="syntax"></a>Синтаксис


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*minutes* 
</dt> <dd>

Количество минут.

</dd> <dt>

*секунд* 
</dt> <dd>

Количество секунд.

</dd> <dt>

*рамки* 
</dt> <dd>

Число кадров.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает время в упакованном формате MSF.

## <a name="remarks"></a>Remarks

Время в формате MSF выражается в виде значения **типа DWORD** с наименьшим значащим байтом, содержащим минуты, следующим наименее значащим байтом, содержащим секунды, и следующим наименьшим значащим байтом, содержащим кадры. Наиболее значимый байт не используется.

Элемент **MCI \_ делает макрос \_ MSF** следующим образом:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Макросы MCI](mci-macros.md)
</dt> </dl>

 

 





