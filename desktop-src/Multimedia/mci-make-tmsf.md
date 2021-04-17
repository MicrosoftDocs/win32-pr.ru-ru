---
title: Макрос MCI_MAKE_TMSF (МЦиапи. h)
description: '\_ \_ Макрос make тмсф создает значение времени в упакованном формате дорожек/минут/секунд/кадров (тмсф) из заданных дорожек, минут, секунд и значений кадров.'
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672890"
---
# <a name="mci_make_tmsf-macro"></a>\_Макрос make \_ тмсф

Макрос **\_ make \_ тмсф** создает значение времени в упакованном формате дорожек/минут/секунд/кадров (тмсф) из заданных дорожек, минут, секунд и значений кадров.

## <a name="syntax"></a>Синтаксис


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*tracks* 
</dt> <dd>

Число дорожек.

</dd> <dt>

*тезис* 
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

Возвращает время в упакованном формате ТМСФ.

## <a name="remarks"></a>Комментарии

Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.

Макрос **\_ make \_ тмсф для MCI** определяется следующим образом:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Макросы MCI](mci-macros.md)
</dt> </dl>

 

 





